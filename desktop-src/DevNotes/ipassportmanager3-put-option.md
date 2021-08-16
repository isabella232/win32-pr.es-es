---
description: Establece un valor Microsoft .NET opción de inicio de sesión de Passport.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3::p ut_Option (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92a1c432df3f3948a85205e26da64073722ba84dd365ebdcaccf3b80521c517c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827243"
---
# <a name="ipassportmanager3put_option-method"></a>IPassportManager3::p ut \_ Option (Método)

Establece un valor Microsoft .NET opción de inicio de sesión de Passport.

> [!Note]  
> El **método put \_ Option** pertenece a la [**interfaz IPassportManager3.**](/previous-versions/ms817681(v=msdn.10)) Este tema complementa la documentación inicial.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* 
</dt> <dd>

Opción de inicio de sesión que se va a establecer. Actualmente, la única opción admitida es iMode.

</dd> <dt>

*newVal* 
</dt> <dd>

**VARIANT** (VT \_ BOOL) que especifica el nuevo valor de la opción. Este valor puede ser True o False.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK cuando el método se realiza correctamente.

## <a name="remarks"></a>Comentarios

Este método se incluye con versiones anteriores del SDK de Passport.

 

 
