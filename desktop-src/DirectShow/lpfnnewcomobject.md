---
description: 'Puntero de función LPFNNewCOMObject: puntero a una función que crea una instancia del objeto .'
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Puntero de función LPFNNewCOMObject (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: f589404cd2a4bf5ff42b331cdf48a978d97e9a274a5fc01a483c804f5878b3eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501955"
---
# <a name="lpfnnewcomobject-function-pointer"></a>Puntero de función LPFNNewCOMObject

Puntero a una función que crea una instancia del objeto .

## <a name="syntax"></a>Sintaxis


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pUnkOuter* 
</dt> <dd>

Puntero a la **interfaz IUnknown** del objeto que agrega el nuevo objeto, si lo hay. Este puntero puede ser **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.** Si se produce un error en el constructor, este parámetro recibe un código de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a una nueva instancia del objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




