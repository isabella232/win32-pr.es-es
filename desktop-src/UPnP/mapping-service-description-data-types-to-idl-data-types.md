---
title: Asignar tipos de datos de descripción de servicio a tipos de datos IDL
description: En la tabla siguiente se muestra la asignación de los tipos de datos XML especificados en una descripción del servicio a los tipos de datos correspondientes utilizados en IDL.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b5fac697c41f54279ecde7436900434895ff23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076185"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a>Asignar tipos de datos de descripción de servicio a tipos de datos IDL

En la tabla siguiente se muestra la asignación de los tipos de datos XML especificados en una descripción del servicio a los tipos de datos correspondientes utilizados en IDL.



| Tipos de datos XML | IDL (tipo de datos)  |
|---------------|----------------|
| bin.base64    | SAFEARRAY      |
| bin.hex       | SAFEARRAY      |
| boolean       | VARIANTE \_ bool  |
| char          | WCHAR \_ t       |
| date          | DATE           |
| dateTime      | DATE           |
| dateTime.tz   | DATE           |
| fixed.14.4    | CY             |
| FLOAT         | FLOAT          |
| i1            | char           |
| i2            | short          |
| i4            | long           |
| int           | long           |
| number        | BSTR           |
| r4            | FLOAT          |
| r8            | double         |
| string        | BSTR           |
| time          | DATE           |
| time.tz       | DATE           |
| ui1           | unsigned char  |
| ui2           | unsigned short |
| ui4           | unsigned long  |
| uri           | BSTR           |
| uuid          | BSTR           |



 

 

 




