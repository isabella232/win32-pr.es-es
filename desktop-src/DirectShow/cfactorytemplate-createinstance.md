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
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266604"
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

Puntero a la interfaz **IUnknown de** agregación.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una instancia del objeto de clase .

## <a name="remarks"></a>Observaciones

El **método IClassFactory::CreateInstance** llama a este método de clase. Este método llama a la función a la que apunta la variable miembro [**CFactoryTemplate::m \_ lpfnNew.**](cfactorytemplate-m-lpfnnew.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




