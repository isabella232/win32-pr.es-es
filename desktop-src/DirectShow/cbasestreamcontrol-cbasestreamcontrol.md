---
description: 'Constructor CBaseStreamControl.CBaseStreamControl: método constructor.'
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: Constructor CBaseStreamControl.CBaseStreamControl (Strmctl.h)
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
ms.openlocfilehash: 4c6521bec65e0182b8eb48eb5d3efe9ea609c6a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095853"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a>Constructor CBaseStreamControl.CBaseStreamControl

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.** Si se produce un error en el constructor, este parámetro recibe un código de error. Si esto ocurre, el objeto no está en un estado válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseStreamControl (clase)**](cbasestreamcontrol.md)
</dt> </dl>

 

 




