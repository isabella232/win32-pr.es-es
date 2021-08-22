---
description: Cuando el cliente haya terminado de comunicarse con cualquier servidor o haya terminado de usar las credenciales adicionales pasadas a la función AcquireCredentialsHandle, el cliente debe llamar a la función FreeCredentialsHandle.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Finalización de una sesión de SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4669d3143b480df20f1a5f1d76e73cc75802766d1db83da9b75d304e256ae4dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008273"
---
# <a name="ending-an-sspi-session"></a>Finalización de una sesión de SSPI

Una vez que el cliente y el servidor han terminado de comunicarse, ambos lados llaman a [**la función DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) con sus respectivos identificadores de contexto. Cuando el cliente haya terminado de comunicarse con cualquier servidor o haya terminado de usar las credenciales adicionales pasadas a la función [**AcquireCredentialsHandle,**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) el cliente debe llamar a la [**función FreeCredentialsHandle.**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) Cuando el servidor está listo para apagarse y antes de descargar el archivo DLL, el servidor debe llamar a **DeleteSecurityContext**.

 

 
