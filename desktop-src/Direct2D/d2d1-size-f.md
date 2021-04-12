---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Almacena un par ordenado de flotantes, normalmente el ancho y el alto de un rectángulo.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489760"
---
# <a name="d2d1_size_f"></a>Tamaño de D2D1 \_ \_ F

Almacena un par ordenado de flotantes, normalmente el ancho y el alto de un rectángulo.


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a>Observaciones

Al igual que los puntos, los tamaños son otro concepto de gráficos importante. En Direct2D, los tamaños se representan mediante las estructuras **D2D1 \_ size \_ F** o [**D2D1 \_ size \_ U**](d2d1-size-u.md) . Ambos contienen un par ordenado de números, normalmente el ancho y el alto de un rectángulo. La **estructura \_ \_ F de tamaño D2D1** contiene un par ordenado de valores **float** y la **estructura \_ \_ U de tamaño de D2D1** contiene un par ordenado de valores **UINT32** .

**D2D1 \_ EL tamaño \_ f** es un nombre nuevo para un tipo ya definido **D2D \_ tamaño \_ F**. Para obtener una lista de los campos proporcionados por **D2D1 \_ size \_ f**, consulte **D2D \_ size \_ f**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2DBaseTypes. h (incluye D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tamaño de D2D \_ \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[**Tamaño de D2D1 \_ \_ U**](d2d1-size-u.md)
</dt> <dt>

[**\_Punto D2D1 \_ 2F**](d2d1-point-2f.md)
</dt> </dl>

 

