---
description: Obtiene la posición en el vector en el que se produjo el cambio.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'Método IVectorChangedEventArgs:: get_Index (IVectorChangedEventArgs. h)'
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
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082126"
---
# <a name="ivectorchangedeventargsget_index-method"></a>IVectorChangedEventArgs:: get \_ index (método)

Obtiene la posición en el vector en el que se produjo el cambio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de out, retval\]
</dt> <dd>

Tipo: **sin signo \** _

Posición de base cero del vector donde se produjo el cambio, si procede.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

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

 

 




