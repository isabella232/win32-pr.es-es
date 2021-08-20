---
description: Todos los procesos (aplicaciones o archivos DLL) que llaman a funciones winsock deben inicializar el uso del archivo DLL de sockets de Windows antes de realizar otras llamadas a funciones winsock. Esto también asegura que Winsock se admite en el sistema.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Inicialización de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aad1dc5bffb09490a963bd86c61c6cc2a857fec45251b38111ab790db8a26e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051523"
---
# <a name="initializing-winsock"></a>Inicialización de Winsock

Todos los procesos (aplicaciones o archivos DLL) que llaman a funciones winsock deben inicializar el uso del archivo DLL de sockets de Windows antes de realizar otras llamadas a funciones winsock. Esto también asegura que Winsock se admite en el sistema.

**Para inicializar Winsock**

1.  Cree un [**objeto WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) denominado wsaData.
    ```C++
    WSADATA wsaData;
    ```

    

2.  Llame [**a WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) y devuelva su valor como un entero y compruebe si hay errores.
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

Se [**llama a la función WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para iniciar el uso de WS2 \_32.dll.

La [**estructura WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) contiene información sobre la implementación Windows Sockets. El parámetro MAKEWORD(2,2) de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) realiza una solicitud para la versión 2.2 de Winsock en el sistema y establece la versión pasada como la versión más alta de compatibilidad de sockets de Windows que el autor de la llamada puede usar.

Paso siguiente para un cliente: [Crear un socket para el cliente](creating-a-socket-for-the-client.md)

Paso siguiente para un servidor: [Crear un socket para el servidor](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Creación de una aplicación Winsock básica](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



