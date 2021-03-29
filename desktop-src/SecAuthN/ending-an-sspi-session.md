---
description: Cuando el cliente ha terminado de comunicarse con cualquier servidor o ha terminado de usar las credenciales adicionales que se pasan a la función AcquireCredentialsHandle, el cliente debe llamar a la función FreeCredentialsHandle.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Finalizar una sesión SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1fdc51ba1c31ae4ac8abb52c6d4c4372a9d161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809349"
---
# <a name="ending-an-sspi-session"></a>Finalizar una sesión SSPI

Una vez que el cliente y el servidor hayan terminado de comunicarse, ambos lados llaman a la función [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) con sus identificadores de contexto respectivos. Cuando el cliente ha terminado de comunicarse con cualquier servidor o ha terminado de usar las credenciales adicionales que se pasan a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , el cliente debe llamar a la función [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) . Cuando el servidor está listo para cerrarse y antes de descargar el archivo DLL, el servidor debe llamar a **DeleteSecurityContext**.

 

 
