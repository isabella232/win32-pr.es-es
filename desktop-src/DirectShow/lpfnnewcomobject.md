---
description: Puntero a una función que crea una instancia del objeto.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Puntero a la función LPFNNewCOMObject (ComBase. h)
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
ms.openlocfilehash: 07c0f8ab961c872c9dc0f92d2fff519b94cd049e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690653"
---
# <a name="lpfnnewcomobject-function-pointer"></a>Puntero a la función LPFNNewCOMObject

Puntero a una función que crea una instancia del objeto.

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

Puntero a la interfaz **IUnknown** del objeto que agrega el nuevo objeto, si existe. Este puntero puede ser **null**.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** . Si se produce un error en el constructor, este parámetro recibe un código de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a una nueva instancia del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




