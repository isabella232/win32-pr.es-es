---
description: Método de constructor.
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: Constructor CMediaControl. CMediaControl (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63b965ff2484d4db7f7de41d8d524bc74c31ac73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680243"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a>Constructor CMediaControl. CMediaControl

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero al nombre del objeto para la depuración.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero al propietario de este objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Asigne el parámetro *pName* en la memoria estática. Este nombre aparece en el terminal de depuración al crear y eliminar el objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 




