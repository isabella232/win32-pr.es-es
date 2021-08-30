---
description: El método Show muestra u oculta el cuadro de diálogo. Este método implementa el método IPropertyPage::Show.
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Método CBasePropertyPage.Show (Cprop.h)
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
ms.openlocfilehash: 4a05a04e1012824e1204318fc3bddaf3e0317c32f3e53fa0e6a5a46f7dd1b50a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103195"
---
# <a name="cbasepropertypageshow-method"></a>CBasePropertyPage.Show (método)

El `Show` método muestra u oculta el cuadro de diálogo. Este método implementa el [método IPropertyPage::Show.](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show)

## <a name="syntax"></a>Sintaxis

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a>Parámetros

*nCmdShow*

Tipo: **[UINT](../winprog/windows-data-types.md)**

Valor que especifica si se debe mostrar u ocultar la ventana. Para obtener más información, vea el [método IPropertyPage::Show.](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show)

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.

| Código devuelto                                                                                  | Descripción                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido.<br/>   |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Error inesperado.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |

## <a name="see-also"></a>Vea también

[CBasePropertyPage (clase)](cbasepropertypage.md)
