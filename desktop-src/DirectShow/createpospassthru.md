---
description: La función CreatePosPassThru crea un objeto CPosPassThru o un objeto CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Función CreatePosPassThru (Ctlutil. h)
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
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680860"
---
# <a name="createpospassthru-function"></a>CreatePosPassThru función)

La `CreatePosPassThru` función crea un objeto [**CPosPassThru**](cpospassthru.md) o un objeto [**CRendererPosPassThru**](crendererpospassthru.md) .

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

Puntero al propietario de este objeto. Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **null**.

</dd> <dt>

*bRenderer* 
</dt> <dd>

Valor booleano que especifica si el filtro es un representador. Use el valor **true** si el filtro es un representador o **false** en caso contrario. Si el valor es **true**, este método crea una instancia de la clase [**CRendererPosPassThru**](crendererpospassthru.md) . Si el valor es **false**, el método crea una instancia de la clase **CPosPassThru** .

</dd> <dt>

*pPin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) en el PIN de entrada del filtro.

</dd> <dt>

*ppPassThru* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz **IUnknown** del objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si se realiza correctamente. De lo contrario, devuelve un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Este método usa la interfaz [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) para crear el objeto. El objeto se carga dinámicamente desde Quartz.dll.

Si la función se ejecuta correctamente, la interfaz **IUnknown** devuelta tiene un recuento de referencias pendiente. El llamador debe liberar la interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




