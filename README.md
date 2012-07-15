# Assert (c) Blake Mizerany and Keith Rarick -- MIT LICENCE

## Assertions for Go tests

## Install

    $ go get github.com/bmizerany/assert

## Use

**point.go**

    package point

    type Point struct {
        x, y int
    }

**point_test.go**


    package point

    import (
        "testing"
        "github.com/bmizerany/assert"
    )

    func TestAsserts(t *testing.T) {
        p1 := Point{1, 1}
        p2 := Point{2, 1}

        assert.Equal(t, p1, p2)
    }

**output**

    --- FAIL: point.TestAsserts
            /Users/blake/code/assert/example/point_test.go:12
            !  Expected: point.Point point.Point{x:1, y:1}
            !  Got:      point.Point point.Point{x:2, y:1}
    FAIL


## Docs

    http://github.com/bmizerany/assert
