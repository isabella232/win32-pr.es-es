---
description: Obtiene la posición en el vector donde se produjo el cambio.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: Método IVectorChangedEventArgs::get_Index (IVectorChangedEventArgs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 72df7f0d46e1e3073262c43064daf58b1fefbf43af913bb7f1b912ed22e67a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560651"
---
# <a name="ivectorchangedeventargsget_index-method"></a>IVectorChangedEventArgs::get \_ Index (método)

Obtiene la posición en el vector donde se produjo el cambio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Tipo: **sin \* signo**

Posición de base cero en el vector donde se produjo el cambio, si procede.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                       |
| Header<br/>                   | <dl> <dt>IVectorChangedEventArgs.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 




