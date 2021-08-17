---
title: Propiedad CounterItem.ScaleFactor
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
ms.openlocfilehash: 794cd84dd62518cc3089b8644f41b5545aeaf547b275c703a4cb87f5fec2b4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883672"
---
# <a name="counteritemscalefactor-property"></a>Propiedad CounterItem.ScaleFactor

Recupera o establece el factor de escala utilizado para representar el valor del contador.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a>Valor de propiedad

Factor de escala usado en la visualización de los valores de contador grafos. Los valores válidos van de -9 a 9 (los valores corresponden a 0,000000001 - 100000000.0).

**Antes de Windows Vista:** Los valores válidos van de -7 a 7 (los valores corresponden a 0,0000001 - 1000000.0).

## <a name="remarks"></a>Comentarios

Establezca esta propiedad solo si desea cambiar el factor de escala predeterminado del contador (cada contador define su propio factor de escala). El valor de esta propiedad se establece en Integer.MaxValue si el contador usa su factor de escala predeterminado para representar los valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





