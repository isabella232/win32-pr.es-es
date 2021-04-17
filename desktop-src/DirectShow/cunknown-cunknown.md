---
description: Método de constructor.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Constructor CUnknown. CUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b500e7f12a2242b6c05367bc061f50680d2d608b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660355"
---
# <a name="cunknowncunknown-constructor"></a>Constructor CUnknown. CUnknown

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Cadena que contiene el nombre del objeto; se usa en el constructor [**CBaseObject**](cbaseobject.md) para la depuración.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero al propietario de este objeto. Si se agrega el objeto, pase un puntero a la interfaz IUnknown del objeto de agregación. De lo contrario, establezca este parámetro en **null**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El objeto se inicializa con un recuento de referencias de cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




