---
title: SNB (Objidl.h)
description: Un bloque de nombre de cadena (SNB) es un puntero a una matriz de punteros a cadenas que termina en un puntero NULL.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- Snb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49a7868912b9d7d1e3d9f3b1f82805e6e285d815eacbc559c887febd23e9e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682785"
---
# <a name="snb"></a>Snb

Un bloque de nombre de cadena (**SNB**) es un puntero a una matriz de punteros a cadenas que termina en un **puntero** NULL. La interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y las llamadas de función que abren objetos de almacenamiento usan bloques de nombres de cadena. Las cadenas apuntan a objetos de almacenamiento o secuencias contenidos que se van a excluir en las llamadas abiertas.


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

**Snb**
</dt> <dd>

\[wire \_ marshal(wireSNB)\]

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **SNB** debe crearse asignando un bloque contiguo de memoria en el que los punteros a cadenas van seguidos de un puntero **NULL,** que luego va seguido de las cadenas reales.

La serialización de **un SNB** se basa en la suposición de que el **SNB** que se pasó se creó de esta manera. Aunque podría almacenarse de otras maneras, el **SNB** creado de esta manera tiene la ventaja de requerir solo una operación de asignación y una liberación de memoria para todas las cadenas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Objidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Objidl.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





