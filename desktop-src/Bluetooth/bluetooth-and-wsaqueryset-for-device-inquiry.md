---
title: Bluetooth y WSAQUERYSET para la consulta de dispositivo
description: Se usa para facilitar la detección de dispositivos y servicios en el espacio de nombres de Bluetooth, \_ BTH NS.
ms.assetid: 0c0d26f7-b6c3-42a9-8c01-118278c381cc
keywords:
- Bluetooth y WSAQUERYSET para la consulta de dispositivos Bluetooth
- WSAQUERYSET Bluetooth, para la consulta de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de7adf8c15907fe539ddac5133df08d68ee7c4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791883"
---
# <a name="bluetooth-and-wsaqueryset-for-device-inquiry"></a>Bluetooth y WSAQUERYSET para la consulta de dispositivo

En Bluetooth, la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) se usa para facilitar la detección de dispositivos y servicios en el espacio de nombres de Bluetooth, NS \_ BTH.

Las funciones [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) y [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usan la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) para obtener información sobre el proceso de consulta de dispositivos. En la tabla siguiente se enumeran y describen los valores de miembro de la estructura **WSAQUERYSET** .

| Miembro                      | Entrada en WSALookupServiceBegin con \_ contenedores LUP especificados                                                                                                                                              | Valor devuelto de WSALookupServiceNext                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**                  | Debe establecerse en **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                       | **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) devuelto por System.                                                                                                                                                                                                                                                                                                                                                        |
| **dwOutputFlags**           | No se utiliza.                                                                                                                                                                                                  | Puede tener una o varias de estas marcas establecidas: **BTHNS \_ result \_ Device \_ Connected** especifica que el dispositivo está conectado.<br/> **BTHNS \_ El \_ dispositivo de resultados \_ recordado** especifica que el dispositivo es un dispositivo recordado. No se autentican todos los dispositivos recordados.<br/> **BTHNS \_ El \_ dispositivo de resultados \_ autenticado** especifica que el dispositivo está autenticado, emparejado o enlazado. Se recuerdan todos los dispositivos autenticados.<br/> |
| **lpszServiceInstanceName** | No se utiliza.                                                                                                                                                                                                  | Nombre para mostrar del dispositivo, que se devolvió originalmente a partir de una operación de solicitud de nombre remoto de Bluetooth y, posiblemente, actualizado por el usuario local. Se devuelve si se especifica **LUP \_ Return \_ Name** .                                                                                                                                                                                                                                         |
| **lpServiceClassId**        | No se utiliza.                                                                                                                                                                                                  | El campo de clase de dispositivo (COD) de Bluetooth de 32 bits asignado al miembro **data1** del GUID. Se devuelve si se especifica el **\_ \_ tipo de valor devuelto LUP** .                                                                                                                                                                                                                                                                                    |
| **lpVersion**               | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszComment**             | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNameSpace**             | Debe ser NS \_ BTH.                                                                                                                                                                                           | Devuelve **\_ BTH NS**.                                                                                                                                                                                                                                                                                                                                                                                                            |
| **lpNSProviderId**          | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**             | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfProtocols**     | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpafpProtocols**          | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszQueryString**         | No se utiliza.                                                                                                                                                                                                  | No se utiliza.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfCsAddrs**       | No se utiliza.                                                                                                                                                                                                  | Indica el número de elementos de la matriz de estructuras de [**\_ información de CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) .                                                                                                                                                                                                                                                                                                                          |
| **lpcsaBuffer**             | No se utiliza.                                                                                                                                                                                                  | Puntero a una estructura de [**\_ información CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) con su miembro **LocalAddr. lpSockaddr** que apunta a una estructura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con la dirección del dispositivo remoto. Se devuelve si se especifica **LUP \_ Return \_ addr** .                                                                                                                                                                  |
| **lpBlob**                  | Opcional. Puede apuntar a una estructura de [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) que apunte a una estructura de [**dispositivo de \_ consulta \_ de BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) que puede limitar la longitud de las operaciones de consulta de dispositivos no almacenadas en caché. | Puntero a una estructura de [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) que apunta a una estructura de [**\_ \_ información del dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) . se devuelve **lpBlob** si se especifica **LUP \_ Return \_ BLOB** . Especifique **LUP \_ Return \_ Name** para recuperar el campo de nombre de la **\_ \_ información del dispositivo BTH**.                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Bluetooth y WSAQUERYSET para Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth y WSAQUERYSET para la consulta de servicio](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Bluetooth y BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Bluetooth y WSALookupServiceNext](bluetooth-and-wsasetservice.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_información del dispositivo BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)
</dt> <dt>

[**\_dispositivo de consulta de BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**información de CSADDR \_**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

