---
description: Además de los certificados y las listas de revocación de certificados (CRL), el almacén de certificados CryptoAPI es compatible con la lista de certificados de confianza (CTL).
ms.assetid: b0f7e7ce-f981-4f3f-83a0-7792224ce0e3
title: Información general de la lista de certificados de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bdbd8b5fdfe4b2d81f3faddb052c16ecf32428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911814"
---
# <a name="certificate-trust-list-overview"></a>Información general de la lista de certificados de confianza

Además de los certificados y [*las listas de revocación de certificados*](../secgloss/c-gly.md) (CRL), el [*almacén de certificados*](../secgloss/c-gly.md) [*CryptoAPI*](../secgloss/c-gly.md) es compatible con la lista de [*certificados de confianza*](../secgloss/c-gly.md) (CTL). CTL es una lista predefinida de elementos firmados por una entidad de confianza. CTL es una lista de [*hashes*](../secgloss/h-gly.md) de certificados o una lista de nombres de archivo. Todos los elementos de la lista se autentican y aprueban por una entidad de firma de confianza. Una estructura de [**\_ contexto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) es similar a las estructuras de contexto de certificado y CRL. Un contexto de CTL puede persistir en el almacén de certificados.

Una CTL CTL es una lista de elementos firmados por una entidad de confianza. La lista de elementos puede ser cualquier cosa, como una lista de hashes de certificados o una lista de nombres de archivo. En la mayoría de los casos, una CTL es una lista de contextos de certificado con hash. La entidad de firma autentica y aprueba todos los elementos de la lista. El uso principal de las CTL es comprobar los mensajes firmados con la CTL como origen de los [*certificados raíz*](../secgloss/r-gly.md)de confianza.

La estructura de [**\_ contexto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) es similar a las estructuras de contexto de certificado y CRL; sin embargo, a diferencia de las estructuras de contexto de CRL y certificado, la estructura de **\_ contexto CTL** contiene un miembro **hCryptMsg** . Este identificador se abre mediante una llamada a cualquiera de las funciones que devuelven una estructura de **\_ contexto CTL** , lo que hace posible el uso de las funciones de mensaje para comprobar la firma de la CTL. Esta comprobación es necesaria para garantizar que una CTL no sea una CTL no replantada por una entidad no autorizada.

Para conocer los procedimientos para crear una CTL firmada y guardarla en un almacén de certificados, vea [crear, firmar y almacenar una CTL](creating-signing-and-storing-a-ctl.md). Consulte también [comprobación de CTL](verifying-a-ctl.md) y [comprobación de mensajes firmados mediante CTL](verifying-signed-messages-by-using-ctls.md) para los procedimientos de comprobación paso a paso.

 

 
