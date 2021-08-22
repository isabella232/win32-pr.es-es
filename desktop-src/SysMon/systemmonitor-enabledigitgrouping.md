---
title: Propiedad SystemMonitor.EnableDigitGrouping
description: Recupera o establece un valor que determina si SYSMON usa la agrupación de dígitos al mostrar valores numéricos.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Propiedad EnableDigitGrouping SysMon
- Propiedad EnableDigitGrouping SysMon , objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad EnableDigitGrouping
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d910e479cc0a957ea5f1332d7fead0f93badd797bfe2d90b26f9914f0c3d863a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882610"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>Propiedad SystemMonitor.EnableDigitGrouping

Recupera o establece un valor que determina si SYSMON usa la agrupación de dígitos al mostrar valores numéricos.

## <a name="syntax"></a>Syntax


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, SYSMON agrupará dígitos al mostrar valores numéricos, por ejemplo, 1214. Si es False, los valores numéricos no se agrupan, por ejemplo, 1214. True es el valor predeterminado.

## <a name="remarks"></a>Comentarios

El símbolo de agrupación de dígitos está localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





