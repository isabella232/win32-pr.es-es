---
title: Sintaxis de cadena (tiempo generalizado)
description: Formato de cadena de tiempo definido por los estándares de ASN.1. | Sintaxis de cadena (tiempo generalizado)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Esquema de AD de sintaxis de cadena (tiempo generalizado)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bf7d965b03b75f4186b807098a5262c402d0c19104a4c09357958b38a77a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580215"
---
# <a name="stringgeneralized-time-syntax"></a>Sintaxis de cadena (tiempo generalizado)

Formato de cadena de tiempo definido por los estándares de ASN.1. Use esta sintaxis para almacenar valores de tiempo en Generalized-Time formato.

El formato de la sintaxis Generalized-Time es "AAAAMMDDHHMMSS.0Z". Un ejemplo de un valor aceptable es "20010928060000.0Z". La "Z" indica que no hay diferencial de tiempo. Active Directory almacena la fecha y hora como Hora media de Greenwich (GMT). Si no se especifica ningún diferencial de hora, GMT es el valor predeterminado.

Si la hora se especifica en una zona horaria que no sea GMT, el diferencial entre la zona horaria y GMT se anexa a la cadena en lugar de "Z" con el formato "AAAAMMDDHHMMSS.0 \[ +/- \] HHMM". Un ejemplo de un valor aceptable es "20010928060000.0+0200". El diferencial se basa en la fórmula: GMT=Local+differential.

Para obtener más información, vea ISO 8601 y X680.



| Entrada | Valor |
|--------------|----------------------------------------------------------------------------|
| Nombre         | String(Generalized-Time)                                                   |
| Identificador de sintaxis    | 2.5.5.11                                                                   |
| Id. de OM        | 24                                                                         |
| Tipo DE MAPI    | SYSTIME                                                                    |
| ADS Type     | ADSTYPE \_ UTC \_ TIME                                                         |
| Tipo de variante | VT \_ DATE                                                                   |
| Tipo sds     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>Vea también

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 
