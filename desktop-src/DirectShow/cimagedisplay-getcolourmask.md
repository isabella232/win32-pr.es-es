---
description: El método GetColourMask recupera las máscaras de color para el formato de presentación actual.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Método CImageDisplay.GetColourMask (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170026"
---
# <a name="cimagedisplaygetcolourmask-method"></a>Método CImageDisplay.GetColourMask

El `GetColourMask` método recupera las máscaras de color para el formato de presentación actual.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMaskRed* 
</dt> <dd>

Puntero a una variable que recibe la máscara de componente rojo.

</dd> <dt>

*pMaskGreen* 
</dt> <dd>

Puntero a una variable que recibe la máscara de componente verde.

</dd> <dt>

*pMaskBlue* 
</dt> <dd>

Puntero a una variable que recibe la máscara de componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageDisplay (clase)**](cimagedisplay.md)
</dt> </dl>

 

 




