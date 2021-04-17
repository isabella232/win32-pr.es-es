---
description: La función DbgCheckModuleLevel comprueba si el registro está habilitado para los tipos de mensaje y el nivel especificados. Se omite en las compilaciones comerciales.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Función DbgCheckModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681053"
---
# <a name="dbgcheckmodulelevel-function"></a>DbgCheckModuleLevel función)

La `DbgCheckModuleLevel` función comprueba si el registro está habilitado para los tipos de mensaje y el nivel especificados. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
BOOL DbgCheckModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipos* 
</dt> <dd>

Combinación bit a bit de uno o varios tipos de mensaje.

</dd> <dt>

*Level* 
</dt> <dd>

Nivel de registro

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el registro de cualquiera de los tipos de mensaje especificados está establecido en el nivel especificado o superior. De lo contrario, devuelve **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 




