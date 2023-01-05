2023/01/05

### 🧑‍💻 **기술블로깅 TechBlog** 🪚

<aside>
💡 4 way-hand shaking

</aside>

* 공부를 위해서 하는 블로깅으로 잘못된 정보가 있을 수 있습니다.

<br><br>

## [ Network ] 4 way-handshaking

**+ TCP란**

---

네트워크 계층 중 전송 계층에서 사용하는 프로토콜

신뢰성을 보장하는 연결형 서비스

<br><br>

**🔩 4 way-handshaking**

---

TCP의 연결을 해제(Connection Termination) 하는 과정

= 클라이언트와 서버가 서로의 통신을 종료하는 과정

<br><br>

**🔩 통신 종료 과정**

---

1. **fin-wait1**
    
    클라이언트가 서버에게 연결을 종료하겠다는 FIN 패킷 전송
    
    서버가 클라이언트에세 우선 ACK 패킷 전송
    
2. **close-wait**
    
    서버는 통신이 끝날 때까지 기다린 후 통신이 끝나면 클라이언트에게 FIN 패킷 전송
    
3. **last-ack**
    
    클라이언트는 ACK 패킷을 서버에게 전송
    
4. **fin-wait2, time-wait**
    
    서버가 보내는 FIN 보다 데이터가 늦게 도착할 수 있기 떄문에 클라이언트는 일정 시간동안 소켓을 열어둔채 패킷을 기다림
    
    이후 연결 종료
    

<br><br>

🔩 **예비 답변**

---

Q. 4 way-handshaking에 대해 설명해주세요.

4 way-handshaking은 클라이언트와 서버가 서로의 통신을 종료하는 4단계 TCP 연결 해제 과정입니다. 

클라이언트가 서버에게 연결을 종료하겠다는 FIN 패킷을 전송하면 서버가 클라이언트에게 ACK 패킷을 전송합니다. 이후 서버는 통신이 끝날 때까지 기다렸다가 통신이 끝난 후 클라이언트에게 FIN 패킷을 전송합니다. 이후 클라이언트는 ACK 패킷을 서버에게 전송하고 서버는 후속 데이터를 기다리는 동안 소켓을 열어둔 후 일정 시간이 지나면 연결을 종료합니다.

<br><br>

🔩 **참고**

---

블로그

[[네트워크] 3-way / 4-way Handshake 란?](https://bangu4.tistory.com/74)

[TCP 3 way handshake, 4 way handshake 알아보기 (feat wireshark)](https://velog.io/@skyepodium/3-way-handshaking-4-way-handshaking)

<br><br>
