---
description: El método TranslateAccelerator indica a la página de propiedades que procese una pulsación de tecla. Este método implementa el método IPropertyPage::TranslateAccelerator.
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: Método CBasePropertyPage.TranslateAccelerator (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc86d50c5692f48c7fb00b45228b13c88c96137473cee3609013f782a0a2d7ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502845"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a>CBasePropertyPage.TranslateAccelerator (método)

El `TranslateAccelerator` método indica a la página de propiedades que procese una pulsación de tecla. Este método implementa el **método IPropertyPage::TranslateAccelerator.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpMsg* 
</dt> <dd>

Puntero a una **estructura MSG** que describe la pulsación de tecla que se debe procesar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Comentarios

Invalide este método si desea proporcionar aceleradores de teclado para la página de propiedades.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




