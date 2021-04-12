---
description: Recupera el valor de una opción específica de inicio de sesión de Microsoft .NET Passport.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'IPassportManager3:: get_Option (método)'
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
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423199"
---
# <a name="ipassportmanager3get_option-method"></a>IPassportManager3:: get ( \_ método de opción)

Recupera el valor de una opción específica de inicio de sesión de Microsoft .NET Passport.

> [!Note]  
> El método **Get \_ Option** pertenece a la interfaz [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) . En este tema se complementa la documentación inicial.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre* \[ de de\]
</dt> <dd>

Opción de inicio de sesión que se va a recuperar. Actualmente, la única opción admitida es "iMode".

</dd> <dt>

*pval* \[ enuncia\]
</dt> <dd>

Un puntero a una **variante** (VT \_ bool) que recibe el valor de la opción. Este valor puede ser true o false.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK cuando el método se ejecuta correctamente.

## <a name="remarks"></a>Observaciones

Este método se incluye con versiones anteriores del SDK de Passport.

 

 
