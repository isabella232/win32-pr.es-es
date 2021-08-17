---
description: Certificate Services admite el uso de certificados tal como se define en la recomendación X.509 de ITU-T (también ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Propiedades del certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48850b812c8a8227f41229ccbaa88259805d61a199d695f4a90d4652a94b99dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771572"
---
# <a name="certificate-properties"></a>Propiedades del certificado

Certificate Services admite el uso de certificados tal como se define en la recomendación [*X.509*](../secgloss/x-gly.md) de ITU-T (también ISO/IEC 9594-8). A continuación se incluyen las propiedades contenidas en un certificado X.509 estándar.



| Campo                                       | Descripción                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión                                     | Número de versión del formato del certificado.                                                                                                                                                                       |
| Número de serie                               | Número de serie del certificado. Este número lo asigna el emisor y es único en la lista del emisor de certificados emitidos.                                                                          |
| Identificador y parámetros del algoritmo         | Algoritmo de firma y cualquier parámetro utilizado por el emisor.                                                                                                                                                      |
| Emisor                                      | Nombre de la [*entidad de certificación*](../secgloss/c-gly.md) que emitió el certificado.                                               |
| No antes (fecha)                           | El certificado no es válido antes de esta fecha.                                                                                                                                                                         |
| Not After (Date)                            | El certificado no es válido después de esta fecha.                                                                                                                                                                          |
| Nombre del firmante                                | Nombre de la persona o entidad a la que se emite el certificado. Este campo también puede incluir la organización, la unidad organizativa, la localidad, el estado o la provincia del destinatario del certificado y el país o región. |
| Parámetros y algoritmos de clave pública de asunto | Algoritmo y parámetros usados para la clave pública [*del sujeto.*](../secgloss/p-gly.md)                                                                       |
| Clave pública del sujeto                          | La clave pública real (una cadena de bits).                                                                                                                                                                           |
| Firma                                   | Firma proporcionada por el emisor.                                                                                                                                                                            |



 

Un certificado puede contener los siguientes elementos, dependiendo de la [*versión X.509*](../secgloss/x-gly.md) del certificado.



| Campo opcional    | Descripción                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador único del emisor  | Se usa para que el nombre del emisor sea inequívoca si lo ha usado más de una entidad. Presente solo en las [*versiones X.509*](../secgloss/x-gly.md) 2.0 o posterior.<br/> |
| Identificador único del asunto | Se usa para que el nombre del sujeto sea inequívoca si lo ha usado más de una entidad. Presente solo en X.509 2.0 o posterior.<br/>                                                                     |
| Extensiones        | Para especificar las propiedades personalizadas deseadas. Se puede incluir cualquier número de campos de extensión en el certificado. Presente solo en la versión X.509 3.0.<br/>                                            |



 

> [!Note]  
> Microsoft Certificate Services emite certificados X.509 versión 3.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de nombre](name-properties.md)
</dt> </dl>

 

 
