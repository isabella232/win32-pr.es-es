---
title: Propiedad ScaleFactor.
description: Recupera o establece el factor de escala que se usa para representar el valor del contador.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Propiedad ScaleFactor SysMon
- Propiedad ScaleFactor SysMon, clase de contraelemento
- Clase de contraelemento SysMon, propiedad ScaleFactor
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666015"
---
# <a name="counteritemscalefactor-property"></a>Propiedad ScaleFactor.

Recupera o establece el factor de escala que se usa para representar el valor del contador.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a>Valor de propiedad

Factor de escala que se usa para mostrar los valores del contador con gráficos. Los valores válidos van de-9 a 9 (los valores corresponden a 0,000000001-100000000,0).

**Antes de Windows Vista:** Los valores válidos van de-7 a 7 (los valores corresponden a 0,0000001-1000000,0).

## <a name="remarks"></a>Observaciones

Establezca esta propiedad únicamente si desea cambiar el factor de escala predeterminado del contador (cada contador define su propio factor de escala). El valor de esta propiedad se establece en Integer. MaxValue si el contador utiliza su factor de escala predeterminado para representar gráficamente los valores.

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

[**SystemMonitor.ScaleToFit**](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





