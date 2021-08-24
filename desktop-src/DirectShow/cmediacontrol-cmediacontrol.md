---
description: 'Constructor CMediaControl.CMediaControl: método constructor.'
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: Constructor CMediaControl.CMediaControl (Ctlutil.h)
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
ms.openlocfilehash: afc31e6d2803632cf2b92d3346fe9d73f3ddb3b5cfab3436fedeee56ab79797a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635055"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a>Constructor CMediaControl.CMediaControl

Método constructor.

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

Puntero al nombre del objeto con fines de depuración.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al propietario de este objeto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Asigne el *parámetro pName* en la memoria estática. Este nombre aparece en el terminal de depuración tras la creación y eliminación del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaControl (clase)**](cmediacontrol.md)
</dt> </dl>

 

 




