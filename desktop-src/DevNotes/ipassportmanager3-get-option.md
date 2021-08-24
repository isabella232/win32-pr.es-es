---
description: Recupera el valor de una opción de Microsoft .NET de inicio de sesión de Passport específica.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: IPassportManager3::get_Option método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5d7260e3c13be21f1cc963e1bca15a6126739a0075b94ee11f07d98901efd39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750045"
---
# <a name="ipassportmanager3get_option-method"></a>IPassportManager3::get \_ (método)

Recupera el valor de una opción de Microsoft .NET de inicio de sesión de Passport específica.

> [!Note]  
> El **método get \_ Option** pertenece a la [**interfaz IPassportManager3.**](/previous-versions/ms817681(v=msdn.10)) Este tema complementa la documentación inicial.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* \[ En\]
</dt> <dd>

Opción de inicio de sesión que se va a recuperar. Actualmente, la única opción admitida es "iMode".

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Puntero a **un VARIANT** (VT \_ BOOL) que recibe el valor de la opción. Este valor puede ser True o False.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK cuando el método se realiza correctamente.

## <a name="remarks"></a>Comentarios

Este método se incluye con versiones anteriores del SDK de Passport.

 

 
