---
title: CounterItem.ScaleFactor, propiedad
description: Recupera o establece el factor de escala utilizado para representar el valor del contador.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Propiedad ScaleFactor SysMon
- Propiedad ScaleFactor SysMon , clase CounterItem
- Clase CounterItem SysMon, propiedad ScaleFactor
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068880"
---
# <a name="counteritemscalefactor-property"></a>CounterItem.ScaleFactor, propiedad

Recupera o establece el factor de escala utilizado para representar el valor del contador.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a>Valor de propiedad

Factor de escala utilizado para mostrar los valores de contador grafos. Los valores válidos oscilan entre -9 y 9 (los valores corresponden a 0,000000001 a 100000000,0).

**Antes de Windows Vista:** Los valores válidos van de -7 a 7 (los valores corresponden a 0,0000001 - 1000000.0).

## <a name="remarks"></a>Observaciones

Establezca esta propiedad solo si desea cambiar el factor de escala predeterminado del contador (cada contador define su propio factor de escala). El valor de esta propiedad se establece en Integer.MaxValue si el contador usa su factor de escala predeterminado para representar los valores.

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

[**SystemMonitor.ScaleToFit**](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





