---
description: Además de los certificados y las listas de revocación de certificados (CRL), el almacén de certificados CryptoAPI admite la lista de certificados de confianza (CTL).
ms.assetid: b0f7e7ce-f981-4f3f-83a0-7792224ce0e3
title: Introducción a la lista de confianza de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7906f02e9af3534445c5b1d6a48c94653feb78b57c71a23acfd9af51477cd050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771111"
---
# <a name="certificate-trust-list-overview"></a>Introducción a la lista de confianza de certificados

Además de los certificados y las listas [*de revocación*](../secgloss/c-gly.md) de certificados (CRL), el almacén de certificados [*CryptoAPI*](../secgloss/c-gly.md) [](../secgloss/c-gly.md) admite la lista de certificados de confianza [](../secgloss/c-gly.md) (CTL). Una CTL es una lista predefinida de elementos firmados por una entidad de confianza. Una CTL es una lista de [*hashes*](../secgloss/h-gly.md) de certificados o una lista de nombres de archivo. Todos los elementos de la lista se autentican y aprueban mediante una entidad de firma de confianza. Una [**estructura CONTEXT \_ de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) es similar a las estructuras de contexto de certificado y CRL. Un contexto de CTL se puede conservar en el almacén de certificados.

Una CTL de CryptoAPI es una lista de elementos firmados por una entidad de confianza. La lista de elementos podría ser cualquier cosa, como una lista de hashes de certificados o una lista de nombres de archivo. En la mayoría de los casos, una CTL es una lista de contextos de certificado con hash. La entidad de firma autentica y aprueba todos los elementos de la lista. El uso principal de las CTL es comprobar los mensajes [*firmados,*](../secgloss/r-gly.md)mediante la CTL como origen de certificados raíz de confianza.

La [**estructura CONTEXT \_ de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) es similar a las estructuras de contexto de certificado y CRL; sin embargo, a diferencia de las estructuras de contexto de certificado y CRL, la estructura CONTEXT de **CTL \_** contiene un **miembro hCryptMsg.** Este identificador se abre mediante una llamada a cualquiera de las funciones que devuelven una estructura CONTEXT de **CTL, \_** lo que permite usar las funciones de mensaje para comprobar la firma de la CTL. Esta comprobación es necesaria para asegurarse de que una CTL no es una CTL desastmbrada por una entidad no fiable.

Para ver los procedimientos para crear una CTL firmada y guardarla en un almacén de certificados, vea Crear, firmar y [almacenar una CTL.](creating-signing-and-storing-a-ctl.md) Consulte también [Comprobación de una CTL y](verifying-a-ctl.md) Comprobación de mensajes firmados mediante [CCL](verifying-signed-messages-by-using-ctls.md) para ver los procedimientos de comprobación paso a paso.

 

 
