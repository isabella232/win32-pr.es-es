---
description: Establece u obtiene el estado de las cuotas de disco del volumen.
title: Propiedad DiskQuotaControl. QuotaState
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
ms.openlocfilehash: 460decc1068642ae797723b31f7350082f591d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497896"
---
# <a name="diskquotacontrolquotastate-property"></a>Propiedad DiskQuotaControl. QuotaState

Establece u obtiene el estado de las cuotas de disco del volumen.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


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
| dqStateEnforce | 2     | Aplique el límite de cuota.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




