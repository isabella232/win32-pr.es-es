---
title: CounterItem.Value, propiedad
description: Recupera el último valor muestreado del contador.
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- Propiedad Value SysMon
- Propiedad Value SysMon , Clase CounterItem
- Clase CounterItem SysMon , propiedad Value
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068877"
---
# <a name="counteritemvalue-property"></a>CounterItem.Value, propiedad

Recupera el último valor muestreado del contador.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property Value As Double
```



## <a name="property-value"></a>Valor de propiedad

Último valor muestreado del contador. El valor es -1 si se produce un error.

## <a name="remarks"></a>Observaciones

Esta es la propiedad predeterminada del [**objeto CounterItem.**](counteritem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**CounterItem.GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





