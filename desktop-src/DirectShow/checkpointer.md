---
description: Comprueba si un puntero es NULL. Si el puntero es NULL, la función o el método en el que aparece la macro devuelve el valor especificado.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro CheckPointr (Wxdebug. h)
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
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660826"
---
# <a name="checkpointer-macro"></a>Macro CheckPointr

Comprueba si un puntero es **null**. Si el puntero es **null**, la función o el método en el que aparece la macro devuelve el valor especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*m* 
</dt> <dd>

Puntero que se va a comprobar.

</dd> <dt>

*direcc* 
</dt> <dd>

Valor que devuelve la función o el método si *p* es **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función circundante devuelve *RET* si *p* es **null**. De lo contrario, la macro no hace que la función circundante devuelva.

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
| Encabezado<br/> | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros de validación de puntero](pointer-validation-macros.md)
</dt> </dl>

 

 




