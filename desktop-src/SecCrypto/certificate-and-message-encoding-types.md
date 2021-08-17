---
description: Muchas de las funciones requieren tipos de codificación de certificados o mensajes.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Tipos de codificación de certificados y mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185be8d3cc781786c93ac809c042c86d3601a45d86eaa39452f0bcbf44203a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771981"
---
# <a name="certificate-and-message-encoding-types"></a>Tipos de codificación de certificados y mensajes

Muchas de las funciones requieren tipos de codificación [*de certificado o mensaje.*](../secgloss/m-gly.md) Este tipo de codificación es **DWORD,** que posiblemente contiene los tipos de codificación de certificado y mensaje. El tipo de codificación del certificado se almacena en la palabra de orden bajo. El tipo de codificación del mensaje se almacena en la palabra de orden superior. Algunas funciones o campos de estructura solo requieren uno de los tipos de codificación, pero siempre es aceptable especificar ambos tipos de codificación. Para obtener un ejemplo en el que se especifican ambos tipos de codificación, [ \# vea includes y \# defines](-includes-and--defines.md).

La siguiente convención de nomenclatura de parámetros se usa para indicar los tipos de codificación necesarios.



| Nombre                       | Comentarios                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dwMsgAndCertEncodingType* | Ambos tipos de codificación son obligatorios.                                                                                                                                                                                                                                                                                       |
| *dwMsgEncodingType*        | Solo se requiere el tipo de codificación del mensaje.                                                                                                                                                                                                                                                                             |
| *dwCertEncodingType*       | Solo se requiere el tipo de codificación de certificado.                                                                                                                                                                                                                                                                         |
| *dwEncodingType*           | Se requiere un tipo de codificación de certificado o mensaje. Si la palabra de orden bajo que contiene el tipo de codificación del certificado es distinta de cero, se usa. De lo contrario, se usa la palabra de orden superior que contiene el tipo de codificación del mensaje. Si se especifican ambos, se usa el tipo de codificación de certificado en la palabra de orden bajo. |



 

Los tipos de codificación definidos actualmente se muestran en la tabla siguiente.



| Tipo de codificación          | Value      |
|------------------------|------------|
| CODIFICACIÓN \_ DE ASN DE \_ CRIP   | 0x00000001 |
| CODIFICACIÓN \_ DE ASN X509 \_    | 0x00000001 |
| CODIFICACIÓN DE \_ \_ ASN PKCS 7 \_ | 0x00010000 |



 

 

 
