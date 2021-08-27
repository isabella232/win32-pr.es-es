---
description: Debe existir una confianza entre el destinatario de un mensaje firmado y el firmante del mensaje.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Comprobación de confianza de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9f88d9c944de8f1c6c40e7657c463740fa94fb94a55a8b9bb0f6e33c69d81f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126825"
---
# <a name="certificate-trust-verification"></a>Comprobación de confianza de certificados

Debe existir una confianza entre el destinatario de un mensaje firmado y el firmante del mensaje. Un método para establecer esta confianza es [*a*](../secgloss/c-gly.md)través de un certificado , un documento electrónico que comprueba que las entidades o personas son quienes dice ser. Un certificado lo emite un tercero de confianza para una entidad de confianza para las otras partes. Por lo tanto, cada destinatario de un mensaje firmado decide si el emisor del certificado del firmante es de confianza. [*CryptoAPI ha*](../secgloss/c-gly.md) implementado una metodología para permitir a los desarrolladores de aplicaciones crear aplicaciones que comprueben automáticamente los certificados con una lista predefinida de certificados o raíces de [*confianza.*](../secgloss/r-gly.md) Esta lista de entidades de confianza (denominada asuntos) se denomina lista [*de certificados de confianza*](../secgloss/c-gly.md) (CTL).

El ejemplo siguiente de uso de una CTL implica a un administrador de intranet (red dentro de la empresa) que quiere controlar solo qué orígenes externos son de confianza. En este caso, el administrador puede crear una lista de certificados o raíces de confianza, firmarla y hacer que la lista esté disponible para todos los clientes de la red en forma de CTL. Una aplicación diseñada para usar esta funcionalidad cryptoAPI solo aceptaría mensajes firmados o software descargado firmado por entidades de la lista.

Para obtener una lista de estas funciones, vea [Funciones de comprobación de certificados](cryptography-functions.md).

 

 
