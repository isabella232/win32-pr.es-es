---
description: Obtiene el tipo de cambio que se produjo en el vector.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: Método IVectorChangedEventArgs::get_CollectionChange (IVectorChangedEventArgs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 2476f9563b4e2a0cabf9babbcfc265ee4f3549416c2fdfda0dbb0f204b7ca9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504815"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a>IVectorChangedEventArgs::get \_ CollectionChange (método)

Obtiene el tipo de cambio que se produjo en el vector.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Tipo: **CollectionChange \***

Valor de la [**enumeración CollectionChange**](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) que describe el cambio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                       |
| Header<br/>                   | <dl> <dt>IVectorChangedEventArgs.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
