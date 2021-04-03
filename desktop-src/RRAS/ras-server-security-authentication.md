---
title: Autenticación de seguridad del servidor RAS
description: Cuando un servidor RAS de Windows NT/Windows 2000 recibe una llamada, invoca la función RasSecurityDialogBegin del archivo DLL de seguridad RAS registrado, si hay alguno.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27184388b418e0fec2a1988fd9e693e942c08e03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075630"
---
# <a name="ras-server-security-authentication"></a>Autenticación de seguridad del servidor RAS

Cuando un servidor RAS de Windows NT/Windows 2000 recibe una llamada, invoca la función [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) del archivo dll de seguridad ras registrado, si hay alguno. Esta llamada notifica a la DLL de seguridad que comienza su autenticación del usuario remoto. El servidor RAS llama a **RasSecurityDialogBegin** antes de realizar la autenticación PPP o ras.

La llamada a [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) pasa la siguiente información al archivo dll de seguridad:

-   Identificador de puerto para identificar la conexión.
-   Punteros a los búferes que se van a usar al comunicarse con el usuario remoto.
-   Puntero a una función [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) que se va a llamar cuando se haya completado la autenticación.

Los punteros de identificador de puerto y de búfer son válidos hasta que el archivo DLL de seguridad llama a [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) para finalizar la transacción de autenticación.

[**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifica al servidor RAS los resultados de la autenticación del archivo dll de seguridad del usuario remoto. Si el archivo DLL de seguridad informa del éxito, el servidor RAS continúa con su autenticación PPP y RAS del usuario remoto. Si el archivo DLL de seguridad informa de que el usuario remoto no ha superado la autenticación, o que se ha producido un error, el servidor RAS cuelga y registra el error o no se ha podido realizar la autenticación en el registro de eventos.

 

 




