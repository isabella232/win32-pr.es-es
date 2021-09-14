---
title: D2D1_SIZE_F (D2DBaseTypes.h)
description: Almacena un par ordenado de flotantes, normalmente el ancho y alto de un rectángulo.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163489"
---
# <a name="d2d1_size_f"></a>D2D1 \_ SIZE \_ F

Almacena un par ordenado de flotantes, normalmente el ancho y alto de un rectángulo.


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a>Observaciones

Al igual que los puntos, los tamaños son otro concepto de gráficos importante. En Direct2D, los tamaños se representan mediante las estructuras **D2D1 \_ SIZE \_ F** [**o D2D1 \_ SIZE \_ U.**](d2d1-size-u.md) Ambos contienen un par ordenado de números, normalmente el ancho y el alto de un rectángulo. La **estructura D2D1 \_ SIZE \_ F** contiene un par ordenado de valores **FLOAT** y la estructura **D2D1 \_ SIZE \_ U** contiene un par ordenado de **valores UINT32.**

**D2D1 \_ SIZE \_ F** es un nuevo nombre para un tipo ya definido **D2D \_ SIZE \_ F**. Para obtener una lista de los campos proporcionados por **D2D1 \_ SIZE \_ F**, vea **D2D \_ SIZE \_ F**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Platform Update for Windows Vista \[ desktop apps \| UWP apps\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y Actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2DBaseTypes.h (incluir D2d1.h)</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D2D \_ SIZE \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[**D2D1 \_ SIZE \_ U**](d2d1-size-u.md)
</dt> <dt>

[**D2D1 \_ POINT \_ 2F**](d2d1-point-2f.md)
</dt> </dl>

 

