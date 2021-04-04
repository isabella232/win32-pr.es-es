---
description: Algunos protocolos requieren varios mensajes de autenticación.
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: Continuación del cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca363489cf87a8fdf2743a8c26a7848c257212e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908601"
---
# <a name="client-continuation"></a>Continuación del cliente

Algunos protocolos requieren varios mensajes de autenticación. En este caso, el cliente analiza la respuesta del servidor y llama a [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) de nuevo con el estado continue de la llamada anterior. El cliente comprueba el estado de devolución de esta llamada y podría ser necesario continuar para otras piernas. Usa la información de *pOutput* para construir un mensaje y lo envía al servidor.

 

 
