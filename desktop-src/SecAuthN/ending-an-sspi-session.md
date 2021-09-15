---
description: Cuando el cliente haya terminado de comunicarse con cualquier servidor o haya terminado de usar las credenciales adicionales pasadas a la función AcquireCredentialsHandle, el cliente debe llamar a la función FreeCredentialsHandle.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Finalización de una sesión de SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1fdc51ba1c31ae4ac8abb52c6d4c4372a9d161
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271463"
---
# <a name="ending-an-sspi-session"></a>Finalización de una sesión de SSPI

Una vez que el cliente y el servidor han terminado de comunicarse, ambos lados llaman a [**la función DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) con sus respectivos identificadores de contexto. Cuando el cliente haya terminado de comunicarse con cualquier servidor o haya terminado de usar las credenciales adicionales pasadas a la función [**AcquireCredentialsHandle,**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) el cliente debe llamar a la [**función FreeCredentialsHandle.**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) Cuando el servidor está listo para apagarse y antes de descargar el archivo DLL, el servidor debe llamar a **DeleteSecurityContext**.

 

 
