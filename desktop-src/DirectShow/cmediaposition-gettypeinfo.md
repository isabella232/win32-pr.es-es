---
description: El método GetTypeInfo recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz.
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Método CMediaPosition. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671556"
---
# <a name="cmediapositiongettypeinfo-method"></a>CMediaPosition. GetTypeInfo, método

El `GetTypeInfo` método recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

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



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




