---
description: Método de constructor.
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: Constructor CBaseStreamControl. CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d325a48476fe2a80b7424850eb71a9d667cb60e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670689"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a>Constructor CBaseStreamControl. CBaseStreamControl

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** . Si se produce un error en el constructor, este parámetro recibe un código de error. Si esto ocurre, el objeto no tiene un estado válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




