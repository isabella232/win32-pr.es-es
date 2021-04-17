---
title: Sintaxis de Object (DS-DN)
description: Cadena que contiene un nombre distintivo (DN).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de objeto (DS-DN)
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535662"
---
# <a name="objectds-dn-syntax"></a>Sintaxis de Object (DS-DN)

Cadena que contiene un nombre distintivo (DN). En el caso de los atributos con esta sintaxis, Active Directory controla los valores de atributo como referencias al objeto identificado por el DN y actualiza automáticamente el valor si el objeto se mueve o se cambia de nombre. En el caso de las consultas que incluyen atributos de sintaxis DN en un filtro, especifique nombres distintivos completos. No se admiten los caracteres comodín (por ejemplo, CN = John \* ).



| Entrada | Value |
|--------------|------------------------------------------------------------------------|
| Nombre         | Object(DS-DN)                                                           |
| IDENTIFICADOR de sintaxis    | 2.5.5.1                                                                |
| IDENTIFICADOR DE OM        | 127                                                                    |
| Tipo MAPI    | OBJECT                                                                 |
| Tipo ADS     | ADSTYPE \_ \_ cadena DN                                                    |
| Tipo Variant | VT \_ BSTR                                                               |
| Tipo de SDS     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>Vea también

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
