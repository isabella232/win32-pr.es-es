---
description: La función CreatePosPassThru crea un objeto CPosPassThru o un objeto CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Función CreatePosPassThru (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0118299bd328d09d77ccbb8d5258b25c0ac57bdc21fc7a47f642374e8be12357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908755"
---
# <a name="createpospassthru-function"></a>Función CreatePosPassThru

La `CreatePosPassThru` función crea un objeto [**CPosPassThru**](cpospassthru.md) o [**un objeto CRendererPosPassThru.**](crendererpospassthru.md)

## <a name="syntax"></a>Sintaxis


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAgg* 
</dt> <dd>

Puntero al propietario de este objeto. Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **NULL.**

</dd> <dt>

*bRenderer* 
</dt> <dd>

Valor booleano que especifica si el filtro es un representador. Use el valor **TRUE si** el filtro es un representador o **FALSE** en caso contrario. Si el valor es **TRUE**, este método crea una instancia de la [**clase CRendererPosPassThru.**](crendererpospassthru.md) Si el valor es **FALSE**, el método crea una instancia de la **clase CPosPassThru.**

</dd> <dt>

*pPin* 
</dt> <dd>

Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) en el pin de entrada del filtro.

</dd> <dt>

*ppPassThru* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la **interfaz IUnknown del** objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente. De lo contrario, devuelve **un valor HRESULT** que indica la causa del error.

## <a name="remarks"></a>Comentarios

Este método usa la [**interfaz ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) para crear el objeto . El objeto se carga dinámicamente desde Quartz.dll.

Si la función se realiza correctamente, la interfaz **IUnknown devuelta** tiene un recuento de referencias pendiente. El autor de la llamada debe liberar la interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 




