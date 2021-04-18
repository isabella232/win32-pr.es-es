---
description: Obtiene el identificador de interfaz de una referencia ágil a un objeto.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'IAgileReference:: Resolve (método)'
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
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705669"
---
# <a name="iagilereferenceresolve-method"></a>IAgileReference:: Resolve (método)

Obtiene el identificador de interfaz de una referencia ágil a un objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* \[ de\]
</dt> <dd>

IDENTIFICADOR de interfaz de la interfaz que se va a recuperar de la referencia ágil. No es necesario que sea el mismo que el de la interfaz registrada.

</dd> <dt>

*ppvObjectReference* \[ out, retval\]
</dt> <dd>

Si se completa correctamente, \* *ppvObjectReference* es un puntero a la interfaz especificada por *riid*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor devuelto                                                                              | Descripción                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ correcto</dt> </dl>          | El método se completó correctamente.<br/>                                  |
| <dl> <dt>E \_ NOinterface</dt> </dl> | La interfaz solicitada no está implementada en el objeto registrado.<br/> |



 

## <a name="remarks"></a>Observaciones

Llame a la función [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) para crear una referencia ágil a un objeto. Llame al método **Resolve** para localizar el objeto en el contenedor en el que se llama a **Resolve** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>            |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




