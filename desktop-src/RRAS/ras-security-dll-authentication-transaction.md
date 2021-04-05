---
title: Transacción de autenticación DLL de seguridad de RAS
description: El servidor RAS de Windows NT/Windows 2000 llama a la función RasSecurityDialogBegin del archivo DLL de seguridad para iniciar la autenticación de un usuario remoto.
ms.assetid: e6549812-d906-4163-b9c8-86f8f1cb1ad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109f6ad5cd3d7b76e30db099a478ffaf562feb32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533429"
---
# <a name="ras-security-dll-authentication-transaction"></a>Transacción de autenticación DLL de seguridad de RAS

El servidor RAS de Windows NT/Windows 2000 llama a la función [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) del archivo dll de seguridad para iniciar la autenticación de un usuario remoto. El servidor RAS está bloqueado y no puede aceptar ninguna otra llamada hasta que **RasSecurityDialogBegin** devuelve. Por esta razón, **RasSecurityDialogBegin** debe copiar los parámetros de entrada, crear un subproceso para realizar la autenticación y volver lo más rápido posible.

El subproceso creado por el archivo DLL de seguridad utiliza las funciones [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) y [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) para comunicarse con el equipo remoto. Estas funciones no están disponibles para la importación estática desde cualquier biblioteca. En su lugar, el archivo DLL de seguridad debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a estas funciones en RASMAN.DLL.

Durante una transacción de autenticación, el administrador de conexiones RAS del equipo remoto muestra una ventana de terminal. El subproceso del archivo DLL de seguridad llama a [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) para enviar un mensaje que se mostrará en la ventana de terminal. A continuación, el subproceso llama a [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) para recibir la entrada que el usuario remoto escribe en la ventana de terminal. El subproceso puede realizar cualquier número de llamadas a **RasSecurityDialogSend** , con cada llamada seguida de una llamada a **RasSecurityDialogReceive** . Después de cada llamada a **RasSecurityDialogReceive**, el subproceso debe llamar a una de las funciones de espera, como [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), para esperar a que se completen las operaciones asincrónicas de envío y recepción. El servidor RAS indica un objeto de evento cuando se ha completado la operación de recepción o cuando ha transcurrido un intervalo de tiempo de espera opcional.

Cuando el subproceso ha terminado de autenticar al usuario remoto, llama a la función [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) . Esta llamada pasa una estructura de [**\_ mensajes de seguridad**](/windows/desktop/api/Rasshost/ns-rasshost-security_message) que contiene los resultados de la transacción de autenticación al servidor RAS. A continuación, el servidor RAS realiza una secuencia de limpieza que incluye una llamada a la función [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) del archivo dll. Esto proporciona al archivo DLL de seguridad una oportunidad para realizar cualquier limpieza necesaria.

El archivo DLL de seguridad puede llamar a la función [**RasSecurityDialogGetInfo**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialoggetinfo) para recuperar información sobre el puerto asociado a una transacción de autenticación. **RasSecurityDialogGetInfo** rellena una estructura de [**\_ \_ información de seguridad de Ras**](/windows/desktop/api/Rasshost/ns-rasshost-ras_security_info) que indica el estado de la última llamada a [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) para el puerto.

 

 