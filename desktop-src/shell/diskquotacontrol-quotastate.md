---
description: Establece u obtiene el estado de las cuotas de disco del volumen.
title: Propiedad DiskQuotaControl.QuotaState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: cb2117237cd3072163447ee80895cbbb8bb854d7ad4424da83854b28ffa96196
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090635"
---
# <a name="diskquotacontrolquotastate-property"></a>Propiedad DiskQuotaControl.QuotaState

Establece u obtiene el estado de las cuotas de disco del volumen.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad se puede establecer en uno de los valores siguientes.



| Estado          | Value | Descripción               |
|----------------|-------|---------------------------|
| dqStateDisable | 0     | Las cuotas de disco están deshabilitadas. |
| dqStateTrack   | 1     | Las cuotas de disco están deshabilitadas. |
| dqStateEnforce | 2     | Exigir límite de cuota.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




