<div class="markdown-body">
#### Microsoft Remote Desktop(RDC) 한영 전환 안됨

  - regedit : 례지스트리 편집기 열기
  - HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout 경로 이동
  - 새로 만들기 -> DWORD(32비트)
     IgnoreRemoteKeyboardLayout : 값 > 1

    - 컴퓨터 재시작
</div>

<div class="markdown-body">
# 핸들러 실행중 취소 - Handler cancel

#### 핸들러 실행

```java
    Handler mHideHandler = new Handler(Looper.getMainLooper());
    mHideHandler.postDelayed(new Runnable() {
        @Override
        public void run() {
            setVisibleInfo(View.GONE);
            setEnable(false);
        }
    }, 10000);
```

#### 핸들러 취소
```java
    mHideHandler.removeCallbacksAndMessages(null);
```
</div>