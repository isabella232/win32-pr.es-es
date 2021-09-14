---
description: La función FindPropertyInstance busca la primera instancia de la propiedad especificada por el parámetro hProperty.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Función FindPropertyInstance (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161151"
---
# <a name="findpropertyinstance-function"></a>Función FindPropertyInstance

La **función FindPropertyInstance** busca la primera instancia de la propiedad especificada por el *parámetro hProperty.*

## <a name="syntax"></a>Sintaxis


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Identificador del marco. El identificador de marco se puede recuperar mediante una llamada a la [función GetFrame.](getframe.md)

</dd> <dt>

*hProperty* \[ En\]
</dt> <dd>

Controle la propiedad que desea buscar. El identificador de propiedad se puede recuperar mediante una llamada a la [función GetProperty.](getproperty.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (es decir, si se encuentra la propiedad ), el valor devuelto es un puntero a la primera instancia de la propiedad.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

Para recuperar la siguiente instancia de la propiedad, llame a [FindPropertyInstanceRestart](findpropertyinstancerestart.md).

[*Los*](e.md) expertos [*y analizadores pueden*](p.md)llamar a **la función FindPropertyInstance.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




