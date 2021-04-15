---
description: Microsoft Digest requiere credenciales de usuario; tanto el cliente como el servidor deben presentar credenciales válidas para poder establecer un contexto de seguridad para el intercambio de mensajes. Los identificadores de credenciales se usan para obtener y presentar credenciales.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Obtención de credenciales de Microsoft Digest SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497285"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a>Obtención de credenciales de Microsoft Digest SSP

Microsoft Digest requiere [*credenciales*](../secgloss/c-gly.md) de usuario; tanto el cliente como el servidor deben presentar credenciales válidas para poder establecer un [*contexto de seguridad*](../secgloss/s-gly.md) para el intercambio de mensajes. Los identificadores de credenciales se usan para obtener y presentar credenciales.

Dado que el identificador de credenciales se usa para almacenar información de configuración, no se puede usar el mismo identificador para las operaciones del lado cliente y del lado servidor. Esto significa que las aplicaciones que admiten conexiones de cliente y de servidor deben obtener un mínimo de dos identificadores de credenciales.

Para obtener un identificador de las credenciales requeridas por Microsoft Digest, llame a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .

En los siguientes ejemplos del lenguaje C se muestra cómo obtener las credenciales.

-   [Obtención de credenciales de Resumen predeterminadas](obtaining-default-digest-credentials.md)
-   [Obtención de credenciales de Resumen alternativas](obtaining-alternate-digest-credentials.md)

 

 
