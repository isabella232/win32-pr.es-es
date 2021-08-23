---
title: Bluetooth y WSAQUERYSET para la consulta de dispositivos
description: Se usa para facilitar la detección de dispositivos y servicios en Bluetooth espacio de nombres, NS \_ BTH.
ms.assetid: 0c0d26f7-b6c3-42a9-8c01-118278c381cc
keywords:
- Bluetooth y WSAQUERYSET para la consulta de dispositivos Bluetooth
- WSAQUERYSET Bluetooth , para la consulta de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a9250670fda52f2ecdc27ffee949b12049b8ec2860b7ee2df23631c4469076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959284"
---
# <a name="bluetooth-and-wsaqueryset-for-device-inquiry"></a>Bluetooth y WSAQUERYSET para la consulta de dispositivos

En Bluetooth, la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) se usa para facilitar la detección de dispositivos y servicios en el espacio de nombres Bluetooth, NS \_ BTH.

Las [**funciones WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) y [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usan la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obtener información sobre el proceso de consulta del dispositivo. En la tabla siguiente se enumeran y describen los valores de miembro de la **estructura WSAQUERYSET.**

| Miembro                      | Entrada a WSALookupServiceBegin con CONTENEDORES LUP \_ especificados                                                                                                                                              | Valor devuelto de WSALookupServiceNext                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**                  | Debe establecerse en **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                       | **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) devuelto por el sistema.                                                                                                                                                                                                                                                                                                                                                        |
| **dwOutputFlags**           | No se usa.                                                                                                                                                                                                  | Puede tener una o varias de estas marcas establecidas: **BTHNS \_ RESULT \_ DEVICE \_ CONNECTED** Especifica que el dispositivo está conectado.<br/> **BTHNS \_ RESULT \_ DEVICE \_ REMEMBERED** Especifica que el dispositivo es un dispositivo recordada. No todos los dispositivos que se recuerden están autenticados.<br/> **BTHNS \_ RESULT \_ DEVICE \_ AUTHENTICATED** Especifica que el dispositivo está autenticado, emparejado o unido. Se recuerda a todos los dispositivos autenticados.<br/> |
| **lpszServiceInstanceName** | No se usa.                                                                                                                                                                                                  | Nombre para mostrar del dispositivo, devuelto originalmente desde una Bluetooth solicitud de nombre remoto y posiblemente actualizado por el usuario local. Se devuelve **si se especifica \_ LUP RETURN \_ NAME.**                                                                                                                                                                                                                                         |
| **lpServiceClassId**        | No se usa.                                                                                                                                                                                                  | Campo de clase Bluetooth de dispositivo (COD) de 32 bits asignado al **miembro Data1** del GUID. Se devuelve **si se especifica \_ LUP RETURN \_ TYPE.**                                                                                                                                                                                                                                                                                    |
| **lpVersion**               | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszComment**             | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNameSpace**             | Debe ser NS \_ BTH.                                                                                                                                                                                           | Devuelve **NS \_ BTH.**                                                                                                                                                                                                                                                                                                                                                                                                            |
| **lpNSProviderId**          | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**             | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfProtocols**     | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpafpProtocols**          | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszQueryString**         | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfCsAddrs**       | No se usa.                                                                                                                                                                                                  | Indica el número de elementos de la matriz de estructuras [**INFO de \_ CSADDR.**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)                                                                                                                                                                                                                                                                                                                          |
| **lpcsaBuffer**             | No se usa.                                                                                                                                                                                                  | Puntero a una estructura INFO de [**CSADDR \_**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) con su miembro **LocalAddr.lpSockaddr** que apunta a una estructura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con la dirección del dispositivo remoto. Se devuelve **si se especifica \_ LUP RETURN \_ ADDR.**                                                                                                                                                                  |
| **lpBlob**                  | Opcional. Puede apuntar a una estructura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) que apunta a una estructura [**\_ BTH QUERY \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) que puede limitar la longitud de las operaciones de consulta de dispositivos no almacenadas en caché. | Puntero a una [**estructura BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) que apunta a una [**estructura \_ BTH DEVICE \_ INFO.**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) **Se devuelve lpBlob** si **se especifica LUP \_ RETURN \_ BLOB.** Especifique **LUP \_ RETURN NAME \_ para** recuperar el campo name de **BTH DEVICE \_ \_ INFO**.                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth y WSAQUERYSET para set service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth y WSAQUERYSET para la consulta de servicios](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Bluetooth y BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Bluetooth y WSALookupServiceNext](bluetooth-and-wsasetservice.md)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH \_ DEVICE \_ INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)
</dt> <dt>

[**BTH \_ QUERY \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**INFORMACIÓN DE \_ CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

