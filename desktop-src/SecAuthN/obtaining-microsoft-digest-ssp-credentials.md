---
description: Las credenciales de usuario son necesarias para Microsoft Digest; Tanto el cliente como el servidor deben presentar credenciales válidas para poder establecer un contexto de seguridad para el intercambio de mensajes. Los identificadores de credenciales se usan para obtener y presentar credenciales.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Obtención de Microsoft Digest de SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea17889331453f009d0d19b7b834e9a4b1301636ec41ef73e6557f79419b461
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921284"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a>Obtención de Microsoft Digest de SSP

Las [*credenciales de*](../secgloss/c-gly.md) usuario son necesarias para Microsoft Digest; Tanto el cliente como el servidor deben presentar credenciales válidas para poder establecer un contexto [*de seguridad para*](../secgloss/s-gly.md) el intercambio de mensajes. Los identificadores de credenciales se usan para obtener y presentar credenciales.

Dado que el identificador de credenciales se usa para almacenar información de configuración, no se puede usar el mismo identificador para las operaciones del lado cliente y del lado servidor. Esto significa que las aplicaciones que admiten conexiones de cliente y servidor deben obtener un mínimo de dos identificadores de credenciales.

Para obtener un identificador de las credenciales requeridas por Microsoft Digest, llame a la [**función AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)

En los siguientes ejemplos del lenguaje C se muestra cómo obtener credenciales.

-   [Obtención de credenciales implícitas predeterminadas](obtaining-default-digest-credentials.md)
-   [Obtención de credenciales de resumen alternativas](obtaining-alternate-digest-credentials.md)

 

 
