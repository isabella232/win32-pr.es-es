---
description: Algunos protocolos requieren varios mensajes de autenticación.
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: Continuación de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007a6fbc3d9fd887b041bf23267ddb804665d733e057c717041ae02b3bb53513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883455"
---
# <a name="client-continuation"></a>Continuación de cliente

Algunos protocolos requieren varios mensajes de autenticación. En este caso, el cliente analiza la respuesta del servidor y llama de nuevo a [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) mediante el estado continue de la llamada anterior. El cliente comprueba el estado de devolución de esta llamada y es posible que deba continuar para obtener más vueltas. Usa la información de *pOutput para* construir un mensaje y lo envía al servidor.

 

 
