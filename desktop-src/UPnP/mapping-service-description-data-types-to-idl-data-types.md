---
title: Asignación de tipos de datos de descripción de servicio a tipos de datos IDL
description: En la tabla siguiente se muestra la asignación de tipos de datos XML especificados en una descripción del servicio a los tipos de datos correspondientes usados en IDL.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a34a5ec9ee092091dc00c7cc420b4474a38d8cba0d41c2691943c7dcd5b35e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347635"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a>Asignación de tipos de datos de descripción de servicio a tipos de datos IDL

En la tabla siguiente se muestra la asignación de tipos de datos XML especificados en una descripción del servicio a los tipos de datos correspondientes usados en IDL.



| Tipos de datos XML | Tipo de datos IDL  |
|---------------|----------------|
| bin.base64    | SAFEARRAY      |
| bin.hex       | SAFEARRAY      |
| boolean       | VARIANT \_ BOOL  |
| char          | wchar \_ t       |
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



 

 

 




