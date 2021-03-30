---
title: Sintaxis de String (tiempo generalizado)
description: Formato de cadena de hora definido por los estándares ASN. 1. | Sintaxis de String (tiempo generalizado)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de cadena (en tiempo generalizado)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280007"
---
# <a name="stringgeneralized-time-syntax"></a>Sintaxis de String (tiempo generalizado)

Formato de cadena de hora definido por los estándares ASN. 1. Use esta sintaxis para almacenar valores de hora en Generalized-Time formato.

El formato de la sintaxis de Generalized-Time es "AAAAMMDDHHMMSS. 0Z". Un ejemplo de un valor aceptable es "20010928060000.0 Z". La "Z" no indica ninguna diferencia horaria. Active Directory almacena la fecha y hora como hora del meridiano de Greenwich (GMT). Si no se especifica ninguna diferencia horaria, GMT es el valor predeterminado.

Si se especifica la hora en una zona horaria distinta de GMT, la diferencia entre la zona horaria y GMT se anexa a la cadena en lugar de a "Z" en la forma "aaaammddhhmmss. 0 \[ +/- \] hhmm". Un ejemplo de un valor aceptable es "20010928060000.0 + 0200". La diferencia se basa en la fórmula: GMT = local + diferencial.

Para obtener más información, vea ISO 8601 y X680.



| Entrada | Value |
|--------------|----------------------------------------------------------------------------|
| Nombre         | String(Generalized-Time)                                                   |
| IDENTIFICADOR de sintaxis    | 2.5.5.11                                                                   |
| IDENTIFICADOR DE OM        | 24                                                                         |
| Tipo MAPI    | SYSTIME                                                                    |
| Tipo ADS     | \_hora UTC de ADSTYPE \_                                                         |
| Tipo Variant | fecha de VT \_                                                                   |
| Tipo de SDS     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>Vea también

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 
