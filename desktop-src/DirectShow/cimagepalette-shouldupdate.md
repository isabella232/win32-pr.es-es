---
description: El método ShouldUpdate determina si es necesario crear una nueva paleta.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Método CImagePalette.ShouldUpdate (Winutil.h)
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
ms.openlocfilehash: c7897e14aec690ec67451fe868b5352e99c9bd513c8c182a47556fe075cffb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916035"
---
# <a name="cimagepaletteshouldupdate-method"></a>CImagePalette.ShouldUpdate (método)

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

Puntero a una [**estructura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contiene la nueva tabla de colores.

</dd> <dt>

*pOldInfo* 
</dt> <dd>

Puntero a una **estructura VIDEOINFOHEADER** que contiene la tabla de colores antigua. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** es necesario actualizar la paleta o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

-   Si ninguna **estructura VIDEOINFOHEADER** contiene una tabla de colores, el método devuelve **FALSE**.
-   Si solo una estructura contiene una tabla de colores, o si *pOldInfo* es **NULL,** el método devuelve **TRUE**.
-   Si ambas estructuras contienen tablas de colores y las entradas de color coinciden, el método devuelve **FALSE.**
-   Si ambas estructuras contienen tablas de colores, pero las entradas de color no coinciden, el método devuelve **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImagePalette (clase)**](cimagepalette.md)
</dt> </dl>

 

 




