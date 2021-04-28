---
description: 'Método CMediaPosition.GetTypeInfo: el método GetTypeInfo recupera la información de tipo del objeto , que luego se puede usar para obtener la información de tipo de una interfaz.'
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Método CMediaPosition.GetTypeInfo (Ctlutil.h)
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
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099143"
---
# <a name="cmediapositiongettypeinfo-method"></a>Método CMediaPosition.GetTypeInfo

El método recupera la información de tipo del objeto , que luego se puede usar `GetTypeInfo` para obtener la información de tipo de una interfaz.

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

Escriba la información que se devolverá. Debe ser cero.

</dd> <dt>

*lcid* 
</dt> <dd>

Identificador de configuración regional.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Dirección de una variable que recibe un **puntero ITypeInfo.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                             | Descripción                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Correcto.<br/>                            |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>               | **Argumento de** puntero NULL.<br/>          |
| <dl> <dt>**TYPE \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | El *parámetro itinfo* no es cero.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaPosition (clase)**](cmediaposition.md)
</dt> </dl>

 

 




