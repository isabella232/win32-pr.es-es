---
title: Propiedad de valor de contraitem. Value
description: Recupera el último valor muestreado del contador.
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- Propiedad de valor SysMon
- Propiedad Value SysMon, clase de contraelemento
- Clase de contraelemento SysMon, propiedad Value
topic_type:
- apiref
api_name:
- CounterItem.Value
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c0d6bd9e1751e34c980bc95f790314017eeb49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666014"
---
# <a name="counteritemvalue-property"></a>Propiedad de valor de contraitem. Value

Recupera el último valor muestreado del contador.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property Value As Double
```



## <a name="property-value"></a>Valor de propiedad

Último valor muestreado del contador. El valor es-1 si se produce un error.

## <a name="remarks"></a>Observaciones

Esta es la propiedad predeterminada del objeto de [**elemento**](counteritem.md) de mismo valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de**](counteritem.md)
</dt> <dt>

[**Peritem. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





