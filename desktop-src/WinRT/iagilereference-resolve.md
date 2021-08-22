---
description: Obtiene el identificador de interfaz de una referencia ágil a un objeto .
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: IAgileReference::Resolve (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 0b58013ba81bb394715a0042f3f3d7435a381fa01f5b985bd9ad81d12122441e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758785"
---
# <a name="iagilereferenceresolve-method"></a>IAgileReference::Resolve (método)

Obtiene el identificador de interfaz de una referencia ágil a un objeto .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* \[ En\]
</dt> <dd>

Identificador de interfaz de la interfaz que se va a recuperar de la referencia ágil. No es necesario que sea igual que la interfaz registrada.

</dd> <dt>

*ppvObjectReference* \[ out, retval\]
</dt> <dd>

Si se completa correctamente, \* *ppvObjectReference es* un puntero a la interfaz especificada por *riid*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor devuelto                                                                              | Descripción                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>          | El método se completó correctamente.<br/>                                  |
| <dl> <dt>E \_ NOINTERFACE</dt> </dl> | La interfaz solicitada no se implementa en el objeto registrado.<br/> |



 

## <a name="remarks"></a>Comentarios

Llame a [**la función RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) para crear una referencia ágil a un objeto . Llame al **método Resolve** para encontrar el objeto en el apartamento en el que se llama **a Resolve.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**RoGetEtoleReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




