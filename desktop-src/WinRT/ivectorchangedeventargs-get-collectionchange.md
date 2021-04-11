---
description: Obtiene el tipo de cambio que se produjo en el vector.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'Método IVectorChangedEventArgs:: get_CollectionChange (IVectorChangedEventArgs. h)'
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
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275410"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a>IVectorChangedEventArgs:: get \_ CollectionChange (método)

Obtiene el tipo de cambio que se produjo en el vector.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de out, retval\]
</dt> <dd>

Tipo: **CollectionChange \** _

Un valor de la enumeración [_ *CollectionChange* *](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) que describe el cambio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                       |
| Encabezado<br/>                   | <dl> <dt>IVectorChangedEventArgs. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
