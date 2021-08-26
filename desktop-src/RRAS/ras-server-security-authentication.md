---
title: Autenticación de seguridad del servidor RAS
description: Cuando un servidor RAS Windows NT/Windows 2000 recibe una llamada, invoca la función RasSecurityDialogBegin del archivo DLL de seguridad RAS registrado, si hay alguno.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532bda51d6e9ee0ea90c900fa974827e1840e7e633caf48fbadec5fe6a701a22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028745"
---
# <a name="ras-server-security-authentication"></a>Autenticación de seguridad del servidor RAS

Cuando un servidor RAS Windows NT/Windows 2000 recibe una llamada, invoca la función [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) del archivo DLL de seguridad RAS registrado, si hay alguno. Esta llamada notifica al archivo DLL de seguridad que inicie su autenticación del usuario remoto. El servidor RAS llama a **RasSecurityDialogBegin antes** de realizar su autenticación PPP o RAS.

La [**llamada RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) pasa la siguiente información al archivo DLL de seguridad:

-   Identificador de puerto para identificar la conexión.
-   Punteros a búferes que se usarán al comunicarse con el usuario remoto.
-   Puntero a una [**función RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) a la que se llamará cuando se haya completado la autenticación.

El identificador de puerto y los punteros de búfer son válidos hasta que el archivo DLL de seguridad llama a [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) para finalizar la transacción de autenticación.

[**RasSecurityDialogComplete notifica**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) al servidor RAS los resultados de la autenticación del archivo DLL de seguridad del usuario remoto. Si el archivo DLL de seguridad informa de que se ha hecho correctamente, el servidor RAS continúa con su autenticación PPP y RAS del usuario remoto. Si la DLL de seguridad informa de que el usuario remoto ha producido un error en la autenticación o de que se ha producido un error, el servidor RAS se cierra y registra el error o la autenticación con errores en el registro de eventos.

 

 




