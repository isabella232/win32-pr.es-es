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
ms.openlocfilehash: 96775678a8d182a3dc88f25fc19b194367c57d92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062489"
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

## <a name="remarks"></a>Observaciones

Asigne el *parámetro pName* en la memoria estática. Este nombre aparece en el terminal de depuración tras la creación y eliminación del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaControl (clase)**](cmediacontrol.md)
</dt> </dl>

 

 




