---
title: Propiedad SystemMonitor. EnableDigitGrouping
description: Recupera o establece un valor que determina si SYSMON usa la agrupación de dígitos al mostrar valores numéricos.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Propiedad EnableDigitGrouping SysMon
- Propiedad EnableDigitGrouping SysMon, objeto SystemMonitor
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
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422342"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>Propiedad SystemMonitor. EnableDigitGrouping

Recupera o establece un valor que determina si SYSMON usa la agrupación de dígitos al mostrar valores numéricos.

## <a name="syntax"></a>Sintaxis


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es true, SYSMON agrupará los dígitos al mostrar valores numéricos, por ejemplo, 1.214. Si es false, los valores numéricos no se agrupan, por ejemplo, 1214. True es el valor predeterminado.

## <a name="remarks"></a>Observaciones

Se localiza el símbolo de agrupación de dígitos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





