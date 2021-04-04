---
description: Servicios de Certificate Server admite el uso de certificados tal y como se define en la recomendación X. 509 de ITU-T (también ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Propiedades del certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908981"
---
# <a name="certificate-properties"></a>Propiedades del certificado

Servicios de Certificate Server admite el uso de certificados tal y como se define en la recomendación [*X. 509*](../secgloss/x-gly.md) de ITU-T (también ISO/IEC 9594-8). A continuación se muestran las propiedades contenidas en un certificado X. 509 estándar.



| Campo                                       | Descripción                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión                                     | Número de versión del formato de certificado.                                                                                                                                                                       |
| Número de serie                               | Número de serie del certificado. Este número lo asigna el emisor y es único en la lista de certificados emitidos del emisor.                                                                          |
| Identificador y parámetros de algoritmo         | Algoritmo de firma y cualquier parámetro utilizado por el emisor.                                                                                                                                                      |
| Emisor                                      | Nombre de la [*entidad de certificación*](../secgloss/c-gly.md) que emitió el certificado.                                               |
| No antes de (fecha)                           | Certificado no válido antes de esta fecha.                                                                                                                                                                         |
| No después de (fecha)                            | Certificado no válido después de esta fecha.                                                                                                                                                                          |
| Nombre del firmante                                | Nombre de la persona o entidad para la que se emite el certificado. Este campo también puede incluir la organización, la unidad organizativa, la localidad, el estado o la provincia del destinatario del certificado, y el país o la región. |
| Algoritmo y parámetros de clave pública de sujeto | El algoritmo y los parámetros utilizados para la [*clave pública*](../secgloss/p-gly.md)del sujeto.                                                                       |
| Clave pública de asunto                          | La clave pública real (una cadena de bits).                                                                                                                                                                           |
| Firma                                   | Firma proporcionada por el emisor.                                                                                                                                                                            |



 

Un certificado puede contener los elementos siguientes, en función de la versión [*X. 509*](../secgloss/x-gly.md) del certificado.



| Campo opcional    | Descripción                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDENTIFICADOR único del emisor  | Se usa para hacer que el nombre del emisor no sea ambiguo si lo ha usado más de una entidad. Presente solo en las versiones [*X. 509*](../secgloss/x-gly.md) 2,0 o posterior.<br/> |
| IDENTIFICADOR único del firmante | Se usa para hacer que el nombre del firmante no sea ambiguo si lo ha utilizado más de una entidad. Presente solo en X. 509 2,0 o posterior.<br/>                                                                     |
| Extensiones        | Para especificar las propiedades personalizadas deseadas. Se puede incluir cualquier número de campos de extensión en el certificado. Presente solo en la versión X. 509 3,0.<br/>                                            |



 

> [!Note]  
> Los servicios de Certificate Server de Microsoft emiten certificados X. 509 versión 3.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de nombre](name-properties.md)
</dt> </dl>

 

 
