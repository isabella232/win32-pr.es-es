---
description: La macro DECLARE \_ IUNKNOWN declara los tres métodos de la interfaz base para una nueva interfaz.
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: DECLARE_IUNKNOWN (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21ba606a5721635398cc9bcf48bba70978e00354188e1a62d83239c853a28b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953214"
---
# <a name="declare_iunknown"></a>DECLARE \_ IUNKNOWN

La **macro DECLARE \_ IUNKNOWN** declara los tres métodos de la interfaz base para una nueva interfaz.

**Sintaxis**

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a>Comentarios

Al crear una nueva interfaz, debe derivarse de **IUnknown**, que tiene tres métodos: **QueryInterface**, **AddRef** y **Release**. Esta macro simplifica el proceso de declaración declarando cada uno de estos métodos para la nueva interfaz.

Esta macro solo funciona con clases que derivan, directa o indirectamente, de la [**clase CUnknown.**](cunknown.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones auxiliares COM**](com-helper-functions.md)
</dt> <dt>

[**CUnknown::GetOwner**](cunknown-getowner.md)
</dt> <dt>

[Cómo implementar IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 




