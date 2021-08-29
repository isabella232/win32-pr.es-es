---
description: Guarda los datos del filtro en la secuencia dada.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Método CPersistStream.Save (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66822a789872ef166d5c5476c496a2543d7896bbba65eddeecf0556ce64ba89f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915575"
---
# <a name="cpersiststreamsave-method"></a>CPersistStream.Save (método)

Guarda los datos del filtro en la secuencia dada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStm* 
</dt> <dd>

Puntero a la secuencia en la que se guardarán los datos.

</dd> <dt>

*fClearDirty* 
</dt> <dd>

Marca que indica si se debe restablecer la marca de desajuste de la secuencia actual; **TRUE** significa restablecerlo. (Cuando se llama al método como parte de una operación De guardar, el valor suele ser **TRUE;** cuando se llama como parte de una operación Guardar como, el valor suele ser **FALSE).**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el **método IPersistStream::Save.** Llama a **WriteInt** con la versión de software, llama a [**CPersistStream::WriteToStream**](cpersiststream-writetostream.md) con la secuencia en *pStm* y restablece **mPS \_ fDirty**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pstream.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPersistStream (clase)**](cpersiststream.md)
</dt> </dl>

 

 




