---
description: La función GetProperty devuelve un identificador a una propiedad determinada.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: Función GetProperty (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171450"
---
# <a name="getproperty-function"></a>Función GetProperty

La **función GetProperty** devuelve un identificador a una propiedad determinada.

## <a name="syntax"></a>Sintaxis


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ En\]
</dt> <dd>

Controle el protocolo.

</dd> <dt>

*PropertyName* \[ En\]
</dt> <dd>

Nombre de la propiedad (por ejemplo, **Suma de comprobación).**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es el identificador de la propiedad .

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

La **función GetProperty** se puede usar para obtener el identificador de propiedad necesario para buscar instancias de la propiedad . Las funciones que se usan para buscar instancias de propiedad son [FindPropertyInstance](findpropertyinstance.md) (que busca la primera instancia) y [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (que busca la instancia siguiente).

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetProperty.**

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

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




