# Домашнее задание к занятию «Уязвимости и атаки на информационные системы» Федоров Дмитрий

### Инструкция по выполнению домашнего задания

<details>

1. Сделайте fork [репозитория c шаблоном решения](https://github.com/netology-code/sys-pattern-homework) к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование этого репозитория к себе на ПК с помощью команды `git clone`.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
   - впишите вверху название занятия и ваши фамилию и имя;
   - в каждом задании добавьте решение в требуемом виде: текст/код/скриншоты/ссылка;
   - для корректного добавления скриншотов воспользуйтесь инструкцией [«Как вставить скриншот в шаблон с решением»](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md);
   - при оформлении используйте возможности языка разметки md. Коротко об этом можно посмотреть в [инструкции по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md).
4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`).
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы задавайте в чате учебной группы и/или в разделе «Вопросы по заданию» в личном кабинете.

</details>

Желаем успехов в выполнении домашнего задания.

------

### Задание 1

Скачайте и установите виртуальную машину Metasploitable: https://sourceforge.net/projects/metasploitable/.

Это типовая ОС для экспериментов в области информационной безопасности, с которой следует начать при анализе уязвимостей.

Просканируйте эту виртуальную машину, используя **nmap**.

Попробуйте найти уязвимости, которым подвержена эта виртуальная машина.

Сами уязвимости можно поискать на сайте https://www.exploit-db.com/.

Для этого нужно в поиске ввести название сетевой службы, обнаруженной на атакуемой машине, и выбрать подходящие по версии уязвимости.

Ответьте на следующие вопросы:

- Какие сетевые службы в ней разрешены?
- Какие уязвимости были вами обнаружены? (список со ссылками: достаточно трёх уязвимостей)
  
*Приведите ответ в свободной форме.*  

<details>
<summary>Ответ</summary>
log file VirtualBox при запуске Metasploitable
   
```sql
00:14:00.668228          ERROR [COM]: aRC=VBOX_E_INVALID_VM_STATE (0x80bb0002) aIID={e36a5081-a82a-40bd-9e4e-42a44d6ce50f} aComponent={MachineWrap} aText={The machine is not mutable, saved or running (state is PoweredOff)}, preserve=false aResultDetail=0
00:14:02.144916          ERROR [COM]: aRC=VBOX_E_OBJECT_NOT_FOUND (0x80bb0001) aIID={5bfd8965-b81b-469f-8649-f717ce97a5d5} aComponent={NvramStoreWrap} aText={The UEFI NVRAM file is not existing for this machine}, preserve=false aResultDetail=0
00:14:02.174115          ERROR [COM]: aRC=VBOX_E_INVALID_VM_STATE (0x80bb0002) aIID={e36a5081-a82a-40bd-9e4e-42a44d6ce50f} aComponent={MachineWrap} aText={The machine is not mutable, saved or running (state is PoweredOff)}, preserve=false aResultDetail=0
00:14:16.955185          Launched VM: 1036622224 pid: 9728 (0x2600) frontend: GUI/Qt name: Metasploitable_0010
00:14:16.986929          ERROR [COM]: aRC=VBOX_E_OBJECT_NOT_FOUND (0x80bb0001) aIID={5bfd8965-b81b-469f-8649-f717ce97a5d5} aComponent={NvramStoreWrap} aText={The UEFI NVRAM file is not existing for this machine}, preserve=false aResultDetail=0
00:14:16.999514          ERROR [COM]: aRC=VBOX_E_INVALID_VM_STATE (0x80bb0002) aIID={e36a5081-a82a-40bd-9e4e-42a44d6ce50f} aComponent={MachineWrap} aText={The machine is not mutable, saved or running (state is PoweredOff)}, preserve=false aResultDetail=0
00:14:21.102344          Platform architecture set to 'x86'
00:14:21.190177          ERROR [COM]: aRC=VBOX_E_OBJECT_NOT_FOUND (0x80bb0001) aIID={5bfd8965-b81b-469f-8649-f717ce97a5d5} aComponent={NvramStoreWrap} aText={The UEFI NVRAM file is not existing for this machine}, preserve=false aResultDetail=0
00:14:21.191608          ERROR [COM]: aRC=VBOX_E_INVALID_VM_STATE (0x80bb0002) aIID={e36a5081-a82a-40bd-9e4e-42a44d6ce50f} aComponent={MachineWrap} aText={The machine is not mutable, saved or running (state is PoweredOff)}, preserve=false aResultDetail=0
00:14:22.407447          Load [C:\Program Files\Oracle\VirtualBox\ExtensionPacks\Oracle_VirtualBox_Extension_Pack\win.amd64\VBoxHostWebcam.DLL] vrc=VINF_SUCCESS
00:14:22.487191          ERROR [COM]: aRC=E_FAIL (0x80004005) aIID={bea3ef5c-de2f-4b74-aa3a-15d6249371a0} aComponent={RecordingSettingsWrap} aText={Recording not started}, preserve=false aResultDetail=0
00:14:32.076838          ERROR [COM]: aRC=VBOX_E_OBJECT_NOT_FOUND (0x80bb0001) aIID={5bfd8965-b81b-469f-8649-f717ce97a5d5} aComponent={NvramStoreWrap} aText={The UEFI NVRAM file is not existing for this machine}, preserve=false aResultDetail=0
00:14:32.086267          ERROR [COM]: aRC=VBOX_E_INVALID_VM_STATE (0x80bb0002) aIID={e36a5081-a82a-40bd-9e4e-42a44d6ce50f} aComponent={MachineWrap} aText={The machine is not mutable, saved or running (state is Starting)}, preserve=false aResultDetail=0
00:14:32.090414          ERROR [COM]: aRC=E_FAIL (0x80004005) aIID={bea3ef5c-de2f-4b74-aa3a-15d6249371a0} aComponent={RecordingSettingsWrap} aText={Recording not started}, preserve=false aResultDetail=0
00:14:32.109175          ERROR [COM]: aRC=VBOX_E_INVALID_VM_STATE (0x80bb0002) aIID={e36a5081-a82a-40bd-9e4e-42a44d6ce50f} aComponent={SessionMachine} aText={The machine is not mutable or saved (state is Starting)}, preserve=false aResultDetail=0
00:14:32.130932          ERROR [COM]: aRC=VBOX_E_INVALID_VM_STATE (0x80bb0002) aIID={e36a5081-a82a-40bd-9e4e-42a44d6ce50f} aComponent={SessionMachine} aText={The machine is not mutable or saved (state is Starting)}, preserve=false aResultDetail=0
00:14:32.132970          Saving settings file "C:\Users\Demon\VirtualBox VMs\Metasploitable_0010\Metasploitable_0010.vbox" with version "1.19-windows"
00:14:32.136718          Finished saving settings file "C:\Users\Demon\VirtualBox VMs\Metasploitable_0010\Metasploitable_0010.vbox"
00:14:32.150367          ERROR [COM]: aRC=VBOX_E_OBJECT_NOT_FOUND (0x80bb0001) aIID={5bfd8965-b81b-469f-8649-f717ce97a5d5} aComponent={NvramStoreWrap} aText={The UEFI NVRAM file is not existing for this machine}, preserve=false aResultDetail=0
00:14:32.152017          ERROR [COM]: aRC=VBOX_E_INVALID_VM_STATE (0x80bb0002) aIID={e36a5081-a82a-40bd-9e4e-42a44d6ce50f} aComponent={MachineWrap} aText={The machine is not mutable, saved or running (state is Starting)}, preserve=false aResultDetail=0
00:14:32.608533          ERROR [COM]: aRC=VBOX_E_OBJECT_NOT_FOUND (0x80bb0001) aIID={7d510820-a678-4730-a862-818dcd3fbed0} aComponent={MediumWrap} aText={Property 'CRYPT/KeyId' does not exist}, preserve=false aResultDetail=0
00:14:32.608894          HostDnsMonitorProxy::GetDomainName: no domain set
00:14:32.608928          HostDnsMonitorProxy::GetNameServers:
00:14:32.608932            name server 1: 192.168.88.1
00:14:32.608935            name server 2: 8.8.8.8
00:14:32.608937            name server 3: 8.8.4.4
00:14:32.608940            name server 4: 77.88.8.8
00:14:32.608942            name server 5: 77.88.8.1
00:14:32.608970          HostDnsMonitorProxy::GetSearchStrings:
00:14:32.608972            no search string entries
00:14:32.626820          ERROR [COM]: aRC=E_FAIL (0x80004005) aIID={bea3ef5c-de2f-4b74-aa3a-15d6249371a0} aComponent={RecordingSettingsWrap} aText={Recording not started}, preserve=false aResultDetail=0
00:14:32.648050          ERROR [COM]: aRC=VBOX_E_OBJECT_NOT_FOUND (0x80bb0001) aIID={5bfd8965-b81b-469f-8649-f717ce97a5d5} aComponent={NvramStoreWrap} aText={The UEFI NVRAM file is not existing for this machine}, preserve=false aResultDetail=0
00:14:32.657871          ERROR [COM]: aRC=VBOX_E_INVALID_VM_STATE (0x80bb0002) aIID={e36a5081-a82a-40bd-9e4e-42a44d6ce50f} aComponent={MachineWrap} aText={The machine is not mutable, saved or running (state is Running)}, preserve=false aResultDetail=0
00:14:35.438986          Saving settings file "C:\Users\Demon\VirtualBox VMs\Metasploitable_0010\Metasploitable_0010.vbox" with version "1.19-windows"
00:14:35.441449          Finished saving settings file "C:\Users\Demon\VirtualBox VMs\Metasploitable_0010\Metasploitable_0010.vbox"
00:14:35.447187          ERROR [COM]: aRC=VBOX_E_OBJECT_NOT_FOUND (0x80bb0001) aIID={5bfd8965-b81b-469f-8649-f717ce97a5d5} aComponent={NvramStoreWrap} aText={The UEFI NVRAM file is not existing for this machine}, preserve=false aResultDetail=0
00:14:35.449567          ERROR [COM]: aRC=VBOX_E_INVALID_VM_STATE (0x80bb0002) aIID={e36a5081-a82a-40bd-9e4e-42a44d6ce50f} aComponent={MachineWrap} aText={The machine is not mutable, saved or running (state is Running)}, preserve=false aResultDetail=0


```

![image](img/01.png)

</details>

---

### Задание 2

Проведите сканирование Metasploitable в режимах SYN, FIN, Xmas, UDP.

Запишите сеансы сканирования в Wireshark.

Ответьте на следующие вопросы:

- Чем отличаются эти режимы сканирования с точки зрения сетевого трафика?
- Как отвечает сервер?

*Приведите ответ в свободной форме.*
<details>
<summary>Ответ</summary>

```sql


```

![image](img/02.png)

</details>

---
