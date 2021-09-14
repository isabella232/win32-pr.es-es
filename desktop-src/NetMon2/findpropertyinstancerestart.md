---
description: Busca la siguiente instancia de la propiedad especificada por el parámetro hProperty.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: Función FindPropertyInstanceRestart (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071562"
---
# <a name="findpropertyinstancerestart-function"></a>Función FindPropertyInstanceRestart

La **función FindPropertyInstanceRestart** busca la siguiente instancia de la propiedad especificada por el *parámetro hProperty.*

## <a name="syntax"></a>Sintaxis


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
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

Identificador de la propiedad que se buscará. El identificador de propiedad se puede recuperar mediante una llamada a la [función GetProperty.](getproperty.md)

</dd> <dt>

*lpRestartKey* \[ En\]
</dt> <dd>

Puntero a la instancia de propiedad utilizada como punto inicial de la búsqueda. Si el *parámetro lpRestartKey* se establece en **NULL,** la búsqueda comienza al principio del marco o al final del marco, dependiendo del valor del *parámetro DirForward.*

Si *lpRestartKey* apunta a **NULL,** la búsqueda comienza al principio del marco si *DirForward* es **TRUE** o al final del marco si el parámetro es **FALSE.**

</dd> <dt>

*DirForward* \[ En\]
</dt> <dd>

Indicador de la dirección de búsqueda. Si el valor es **TRUE**, la búsqueda se mueve desde la ubicación actual hasta el final del marco. Si el valor es **FALSE,** la búsqueda se mueve desde la ubicación actual hasta el principio del marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es el **siguiente LPPROPERTYINST válido.**

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función FindPropertyInstanceRestart.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[GetFrame](getframe.md)
</dt> <dt>

[Getproperty](getproperty.md)
</dt> </dl>

 

 




