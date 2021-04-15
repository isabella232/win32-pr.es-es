---
description: Muchas de las funciones requieren tipos de codificación de mensajes o de certificados.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Tipos de codificación de mensajes y certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497273"
---
# <a name="certificate-and-message-encoding-types"></a>Tipos de codificación de mensajes y certificados

Muchas de las funciones requieren tipos de [*codificación de mensajes*](../secgloss/m-gly.md)o de certificados. Este tipo de codificación es un **valor DWORD**, que posiblemente contiene los tipos de codificación de mensajes y de certificado. El tipo de codificación del certificado se almacena en la palabra de orden inferior. El tipo de codificación del mensaje se almacena en la palabra de orden superior. Algunas funciones o campos de estructura requieren solo uno de los tipos de codificación, pero siempre es aceptable especificar ambos tipos de codificación. Para obtener un ejemplo en el que se especifican ambos tipos de codificación, vea [ \# includes y \# defines](-includes-and--defines.md).

La siguiente Convención de nomenclatura de parámetros se usa para indicar los tipos de codificación necesarios.



| Nombre                       | Comentarios                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dwMsgAndCertEncodingType* | Ambos tipos de codificación son obligatorios.                                                                                                                                                                                                                                                                                       |
| *dwMsgEncodingType*        | Solo se requiere el tipo de codificación del mensaje.                                                                                                                                                                                                                                                                             |
| *dwCertEncodingType*       | Solo se requiere el tipo de codificación de certificado.                                                                                                                                                                                                                                                                         |
| *dwEncodingType*           | Se requiere un mensaje o un tipo de codificación de certificado. Si la palabra de orden inferior que contiene el tipo de codificación de certificado es distinto de cero, se usa. De lo contrario, se usa la palabra de orden superior que contiene el tipo de codificación de mensajes. Si se especifican ambos, se usa el tipo de codificación del certificado en la palabra de orden inferior. |



 

En la tabla siguiente se muestran los tipos de codificación definidos actualmente.



| Tipo de codificación          | Value      |
|------------------------|------------|
| CIFRAdo de la \_ \_ codificación ASN   | 0x00000001 |
| \_Codificación ASN de X509 \_    | 0x00000001 |
| CODIFICACIÓN de ASN de PKCS \_ 7 \_ \_ | 0x00010000 |



 

 

 
