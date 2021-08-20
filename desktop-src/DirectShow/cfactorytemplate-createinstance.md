---
description: El método CreateInstance llama a la función de creación de objetos para la clase .
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Método CFactoryTemplate.CreateInstance (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 816d690a7e57df83b3f521f4591c3334269d0fccebbaeac480e7aacb46253273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074219"
---
# <a name="cfactorytemplatecreateinstance-method"></a>Método CFactoryTemplate.CreateInstance

El `CreateInstance` método llama a la función de creación de objetos para la clase .

## <a name="syntax"></a>Sintaxis


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Punk* 
</dt> <dd>

Puntero a la interfaz **IUnknown de agregación.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una instancia del objeto de clase.

## <a name="remarks"></a>Comentarios

El **método IClassFactory::CreateInstance** llama a este método de clase. Este método llama a la función a la que apunta la variable miembro [**CFactoryTemplate::m \_ lpfnNew.**](cfactorytemplate-m-lpfnnew.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




