---
description: Debe existir una confianza entre el destinatario de un mensaje firmado y el firmante del mensaje.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Comprobación de certificados de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b711e0a86dcc5ae9cdedea278d6a3a698dfd633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688098"
---
# <a name="certificate-trust-verification"></a>Comprobación de certificados de confianza

Debe existir una confianza entre el destinatario de un mensaje firmado y el firmante del mensaje. Un método para establecer esta confianza es a través de un [*certificado*](../secgloss/c-gly.md), un documento electrónico que comprueba que las entidades o personas son quienes dicen ser. Un tercero que confía en las dos partes de un certificado emite un certificado a una entidad. Por lo tanto, cada destinatario de un mensaje firmado decide si el emisor del certificado del firmante es de confianza. [*CryptoAPI*](../secgloss/c-gly.md) ha implementado una metodología que permite a los desarrolladores de aplicaciones crear aplicaciones que comprueban automáticamente los certificados en una lista predefinida de certificados o [*raíces*](../secgloss/r-gly.md)de confianza. Esta lista de entidades de confianza (denominadas asuntos) se denomina [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL).

El siguiente ejemplo de uso de una CTL implica a un administrador de intranet (red interna) que desea controlar con qué orígenes externos son de confianza. En este caso, el administrador puede crear una lista de certificados o raíces de confianza, firmarlo y hacer que la lista esté disponible para todos los clientes de la red en forma de CTL. Una aplicación diseñada para usar esta funcionalidad de CryptoAPI solo aceptará mensajes firmados o software descargado firmado por entidades de la lista.

Para obtener una lista de estas funciones, consulte [funciones de comprobación de certificados](cryptography-functions.md).

 

 
