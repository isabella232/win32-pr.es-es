---
description: Establece una opción específica de inicio de sesión de Microsoft .NET Passport.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3::p ut_Option método
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
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998100"
---
# <a name="ipassportmanager3put_option-method"></a>IPassportManager3::p \_ método de opción UT

Establece una opción específica de inicio de sesión de Microsoft .NET Passport.

> [!Note]  
> El método **Put \_ Option** pertenece a la interfaz [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) . En este tema se complementa la documentación inicial.

 

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

**Variant** (VT \_ bool) que especifica el nuevo valor de la opción. Este valor puede ser true o false.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK cuando el método se ejecuta correctamente.

## <a name="remarks"></a>Observaciones

Este método se incluye con versiones anteriores del SDK de Passport.

 

 
