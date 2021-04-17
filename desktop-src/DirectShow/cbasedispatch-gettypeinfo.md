---
description: El método GetTypeInfo recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Método CBaseDispatch. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f63d79327d2f2bf2a60f06e0290aa34891e78ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660583"
---
# <a name="cbasedispatchgettypeinfo-method"></a>CBaseDispatch. GetTypeInfo, método

El `GetTypeInfo` método recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* 
</dt> <dd>

Referencia a un identificador de interfaz (IID) que especifica la interfaz.

</dd> <dt>

*itinfo* 
</dt> <dd>

Información de tipo que se va a devolver. Debe ser cero.

</dd> <dt>

*lcid* 
</dt> <dd>

Identificador de configuración regional.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Dirección de una variable que recibe un puntero **ITypeInfo** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                             | Descripción                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                    | Correcto.<br/>                            |
| <dl> <dt>**\_puntero E**</dt> </dl>               | Argumento de puntero **nulo** .<br/>          |
| <dl> <dt>**Escriba \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | El parámetro *itinfo* no es cero.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método se comporta como el método **IDispatch:: GetTypeInfo** . Sin embargo, incluye un parámetro adicional, *riid*, que especifica la interfaz cuya información de tipo se va a recuperar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 




