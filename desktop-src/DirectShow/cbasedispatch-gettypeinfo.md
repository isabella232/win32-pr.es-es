---
description: 'Método CBaseDispatch.GetTypeInfo: el método GetTypeInfo recupera la información de tipo del objeto , que luego se puede usar para obtener la información de tipo de una interfaz.'
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Método CBaseDispatch.GetTypeInfo (Ctlutil.h)
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
ms.openlocfilehash: 294b9758aa79ab033c1e3cf8932056ca10e7bf2424de97a1cf9f3b509f1906bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076685"
---
# <a name="cbasedispatchgettypeinfo-method"></a>Método CBaseDispatch.GetTypeInfo

El método recupera la información de tipo para el objeto , que luego se puede usar `GetTypeInfo` para obtener la información de tipo de una interfaz.

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



 

## <a name="remarks"></a>Comentarios

Este método se comporta como **el método IDispatch::GetTypeInfo.** Sin embargo, incluye un parámetro adicional, *riid*, que especifica la interfaz para la que se va a recuperar información de tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseDispatch (clase)**](cbasedispatch.md)
</dt> </dl>

 

 




