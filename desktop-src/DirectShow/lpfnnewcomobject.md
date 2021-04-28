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
ms.openlocfilehash: f3ea5bc172bc22f7aa9dce1f348bba552520565f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116533"
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

Puntero a **la interfaz IUnknown** del objeto que agrega el nuevo objeto, si lo hay. Este puntero puede ser **NULL.**

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
| Encabezado<br/> | <dl> <dt>Combase.h (incluir Streams.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




