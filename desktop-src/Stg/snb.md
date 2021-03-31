---
title: SNB (Objidl. h)
description: Un bloque de nombre de cadena (SNB) es un puntero a una matriz de punteros a cadenas, que finaliza en un puntero nulo.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- SNB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996164"
---
# <a name="snb"></a>SNB

Un bloque de nombre de cadena (**SNB**) es un puntero a una matriz de punteros a cadenas, que finaliza en un puntero **nulo** . Los bloques de nombre de cadena se utilizan en la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y las llamadas a funciones que abren objetos de almacenamiento. Las cadenas apuntan a objetos de almacenamiento contenidos o flujos que se van a excluir en las llamadas abiertas.


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

**SNB**
</dt> <dd>

\[\_serialización de cable (wireSNB)\]

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **SNB** debe crearse mediante la asignación de un bloque de memoria contiguo en el que los punteros a cadenas van seguidos de un puntero **nulo** , que a continuación va seguido de las cadenas reales.

El cálculo de referencias de un **SNB** se basa en la suposición de que el **SNB** que se pasó se creó de este modo. Aunque podría almacenarse de otras maneras, el **SNB** creado de esta manera tiene la ventaja de requerir solo una operación de asignación y una liberación de memoria para todas las cadenas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Objidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Objidl. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





