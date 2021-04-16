---
description: El método ShouldUpdate determina si es necesario crear una nueva paleta.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Método CImagePalette. ShouldUpdate (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670491"
---
# <a name="cimagepaletteshouldupdate-method"></a>CImagePalette. ShouldUpdate, método

El `ShouldUpdate` método determina si es necesario crear una nueva paleta.

## <a name="syntax"></a>Sintaxis


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNewInfo* 
</dt> <dd>

Puntero a una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contiene la nueva tabla de colores.

</dd> <dt>

*pOldInfo* 
</dt> <dd>

Puntero a una estructura **VIDEOINFOHEADER** que contiene la tabla de colores antigua. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la paleta debe actualizarse o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

-   Si ninguna de las estructuras **VIDEOINFOHEADER** contiene una tabla de colores, el método devuelve **false**.
-   Si solo una estructura contiene una tabla de colores, o si *pOldInfo* es **null**, el método devuelve **true**.
-   Si ambas estructuras contienen tablas de color y las entradas de color coinciden, el método devuelve **false**.
-   Si ambas estructuras contienen tablas de color, pero las entradas de color no coinciden, el método devuelve **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




