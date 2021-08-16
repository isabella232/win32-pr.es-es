---
title: Transacción de autenticación DE DLL de seguridad ras
description: Windows NT/Windows servidor RAS 2000 llama a la función RasSecurityDialogBegin del archivo DLL de seguridad para iniciar una autenticación de un usuario remoto.
ms.assetid: e6549812-d906-4163-b9c8-86f8f1cb1ad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea463c56d96cad13fb55a2b6e0bbdfc154518ba012e4c71c6ab8bdd3213cd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789481"
---
# <a name="ras-security-dll-authentication-transaction"></a>Transacción de autenticación DE DLL de seguridad ras

Windows NT/Windows servidor RAS 2000 llama a la función [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) del archivo DLL de seguridad para iniciar una autenticación de un usuario remoto. El servidor RAS está bloqueado y no puede aceptar ninguna otra llamada hasta que **rasSecurityDialogBegin** vuelva. Por este motivo, **RasSecurityDialogBegin** debe copiar los parámetros de entrada, crear un subproceso para realizar la autenticación y devolver lo antes posible.

El subproceso creado por el archivo DLL de seguridad usa las funciones [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) y [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) para comunicarse con el equipo remoto. Estas funciones no están disponibles para la importación estática desde ninguna biblioteca. En su lugar, el archivo DLL de seguridad debe usar las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a estas funciones en RASMAN.DLL.

Durante una transacción de autenticación, el administrador de conexiones RAS en el equipo remoto muestra una ventana de terminal. El subproceso del archivo DLL de seguridad llama a [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) para enviar un mensaje que se mostrará en la ventana del terminal. A continuación, el subproceso [**llama a RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) para recibir la entrada que el usuario remoto tipos en la ventana del terminal. El subproceso puede realizar cualquier número de **llamadas RasSecurityDialogSend,** con cada llamada seguida de una **llamada RasSecurityDialogReceive.** Después de cada llamada a **RasSecurityDialogReceive**, el subproceso debe llamar a una de las funciones de espera, como [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), para esperar a que se completen las operaciones asincrónicas de envío y recepción. El servidor RAS señala un objeto de evento cuando se ha completado la operación de recepción o cuando ha transcurrido un intervalo de tiempo de espera opcional.

Cuando el subproceso ha terminado de autenticar al usuario remoto, llama a la [**función RasSecurityDialogComplete.**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) Esta llamada pasa al servidor RAS una [**estructura SECURITY \_ MESSAGE**](/windows/desktop/api/Rasshost/ns-rasshost-security_message) que contiene los resultados de la transacción de autenticación. A continuación, el servidor RAS realiza una secuencia de limpieza que incluye una llamada a la función [**RasSecurityDialogEnd del**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) archivo DLL. Esto ofrece al archivo DLL de seguridad la oportunidad de realizar cualquier limpieza necesaria.

El archivo DLL de seguridad puede llamar a [**la función RasSecurityDialogGetInfo**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialoggetinfo) para recuperar información sobre el puerto asociado a una transacción de autenticación. **RasSecurityDialogGetInfo** rellena una estructura DE INFORMACIÓN DE SEGURIDAD de RAS que indica el estado de la última [**llamada RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) para el puerto. [**\_ \_**](/windows/desktop/api/Rasshost/ns-rasshost-ras_security_info)

 

 