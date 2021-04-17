---
description: Guarda los datos del filtro en la secuencia especificada.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Método CPersistStream. Save (pStream. h)
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
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670996"
---
# <a name="cpersiststreamsave-method"></a>CPersistStream. Save (método)

Guarda los datos del filtro en la secuencia especificada.

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

Puntero a la secuencia en la que se van a guardar los datos.

</dd> <dt>

*fClearDirty* 
</dt> <dd>

Marca que indica si se debe restablecer la marca de modificado del flujo actual; **True** significa que se va a restablecer. (Cuando se llama al método como parte de una operación de guardar, el valor suele ser **true**; cuando se llama como parte de una operación Guardar como, el valor suele ser **false**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método **IPersistStream:: Save** . Llama a **WriteInt** con la versión de software, llama a [**CPersistStream:: WriteToStream**](cpersiststream-writetostream.md) con la secuencia en *pStm* y restablece **mPS \_ fDirty**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PStream. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




