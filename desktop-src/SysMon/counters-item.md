---
title: Counters.Item, propiedad
description: Recupera la instancia de CounterItem especificada de la colección.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Propiedad De elemento SysMon
- Propiedad De elemento SysMon , Clase Counters
- Clase Counters SysMon , propiedad Item
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 451a6e43714a9ca5ee8e64bf48fdf80aa9e5a9d7b99db8f78f997eba9404e284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883413"
---
# <a name="countersitem-property"></a>Counters.Item, propiedad

Recupera la instancia de [**CounterItem especificada**](counteritem.md) de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a>Valor de propiedad

[**Instancia counterItem**](counteritem.md) que corresponde al valor de índice especificado.

## <a name="exceptions"></a>Excepciones



| Tipo de excepción                                  | Condición                         |
|-------------------------------------------------|-----------------------------------|
| **System.Runtime.InteropServices.COMException** | El índice especificado no es válido. |



 

## <a name="remarks"></a>Comentarios

Esta es la propiedad predeterminada del [**objeto Counters.**](counters.md)

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

[**Counters**](counters.md)
</dt> </dl>

 

 





