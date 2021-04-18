---
description: 'El método Show muestra u oculta el cuadro de diálogo. Este método implementa el método IPropertyPage:: show.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Método CBasePropertyPage. Show (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671267"
---
# <a name="cbasepropertypageshow-method"></a>CBasePropertyPage. Show (método)

El `Show` método muestra u oculta el cuadro de diálogo. Este método implementa el método [IPropertyPage:: show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .

## <a name="syntax"></a>Sintaxis

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a>Parámetros

*nCmdShow*

Tipo: **[uint](../winprog/windows-data-types.md)**

Valor que especifica si se debe mostrar u ocultar la ventana. Para obtener más información, vea el método [IPropertyPage:: show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.

| Código devuelto                                                                                  | Descripción                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido.<br/>   |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Error inesperado.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |

## <a name="see-also"></a>Vea también

[Clase CBasePropertyPage](cbasepropertypage.md)
