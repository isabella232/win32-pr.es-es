---
description: La función FindPropertyInstance busca la primera instancia de la propiedad especificada por el parámetro hProperty.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Función FindPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666289"
---
# <a name="findpropertyinstance-function"></a>FindPropertyInstance función)

La función **FindPropertyInstance** busca la primera instancia de la propiedad especificada por el parámetro *hProperty* .

## <a name="syntax"></a>Sintaxis


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador del marco. El identificador del marco se puede recuperar mediante una llamada a la función [GetFrame](getframe.md) .

</dd> <dt>

*hProperty* \[ de\]
</dt> <dd>

Identificador de la propiedad que se desea buscar. El identificador de propiedad se puede recuperar mediante una llamada a la función [GetProperty](getproperty.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (es decir, si se encuentra la propiedad), el valor devuelto es un puntero a la primera instancia de la propiedad.

Si la función no se realiza correctamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

Para recuperar la siguiente instancia de la propiedad, llame a [FindPropertyInstanceRestart](findpropertyinstancerestart.md).

Los [*expertos*](e.md) y [*analizadores*](p.md)pueden llamar a la función **FindPropertyInstance** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




