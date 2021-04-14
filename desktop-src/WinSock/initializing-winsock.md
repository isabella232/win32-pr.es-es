---
description: Todos los procesos (aplicaciones o archivos dll) que llaman a funciones Winsock deben inicializar el uso de la DLL de Windows Sockets antes de realizar otras llamadas a funciones Winsock. Esto también garantiza que Winsock sea compatible con el sistema.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Inicializando Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541571"
---
# <a name="initializing-winsock"></a>Inicializando Winsock

Todos los procesos (aplicaciones o archivos dll) que llaman a funciones Winsock deben inicializar el uso de la DLL de Windows Sockets antes de realizar otras llamadas a funciones Winsock. Esto también garantiza que Winsock sea compatible con el sistema.

**Para inicializar Winsock**

1.  Cree un objeto [**wsadata (**](/windows/desktop/api/winsock/ns-winsock-wsadata) denominado wsadata (.
    ```C++
    WSADATA wsaData;
    ```

    

2.  Llame a [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) y devuelva su valor como un entero y compruebe si hay errores.
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

Se llama a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para iniciar el uso de WS2 \_32.dll.

La estructura [**wsadata (**](/windows/desktop/api/winsock/ns-winsock-wsadata) contiene información sobre la implementación de Windows Sockets. El parámetro MAKEWORD (2, 2) de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) realiza una solicitud de la versión 2,2 de Winsock en el sistema y establece la versión pasada como la versión más alta de compatibilidad de Windows Sockets que puede usar el autor de la llamada.

Siguiente paso para un cliente: [crear un socket para el cliente](creating-a-socket-for-the-client.md)

Siguiente paso para un servidor: [crear un socket para el servidor](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Crear una aplicación de Winsock básica](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



