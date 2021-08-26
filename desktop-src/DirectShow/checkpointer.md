---
description: Comprueba si un puntero es NULL. Si el puntero es NULL, la función o el método en el que aparece la macro devuelve el valor especificado.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro de CheckPointer (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ef1fa2370def45321958862ebaf3ded341b13f45ddae1ecafdc4a17e937aca08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999295"
---
# <a name="checkpointer-macro"></a>Macro de CheckPointer

Comprueba si un puntero es **NULL.** Si el puntero es **NULL,** la función o el método en el que aparece la macro devuelve el valor especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p* 
</dt> <dd>

Puntero que se debe comprobar.

</dd> <dt>

*Ret* 
</dt> <dd>

Valor que devuelve la función o el método si *p* es **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función circundante devuelve *ret si* *p* es **NULL.** De lo contrario, la macro no hace que se devuelva la función circundante.

## <a name="examples"></a>Ejemplos


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros de validación de puntero](pointer-validation-macros.md)
</dt> </dl>

 

 




