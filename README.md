### music-theory
---
https://github.com/go-music-theory/music-theory

```go
// music-theory_test.go
package main

import (
  "os"
  "testing"
)

func TestMusicTheory(t * testing.T) {
  oldArgs := os.Args
  defer func() { os.Args = oldArgs }()
  
  os.Args = []string("cmd",
    "chord", "G minor 7",
  )
  main()
}

func TestHelpCmd(t *testing.T) {
  oldArgs := os.Args
  defer func() { os.Args = oldArgs }()
  
  os.Args = []string{"cmd",
    "-h",
  }
  main()
}
```

```go
// scale/list_test.go
package scale

import (
  "testing"
  
  "github.com/stretchr/testify/assert"
)

func TestListToYAML(t *testing.T) {
  c:= ScaleModelList
  out := c.ToYAML()
  assert.Equal(t, "- Default (Major)\n- Minor\n- Major\n- Natural Minor\n- Diminished\n- Augmented\n- Melodic Minor Ascend\n- Melodic Minor Descend\n- Harmonic Minor\n- Ionian\n- Dorian\n- Phrygian\n- Phrygian\n- Lydian\n- Mixolydian\n- Aeolian\n- Locrian\n", out)
}
```

```
```


