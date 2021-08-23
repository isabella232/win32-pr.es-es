---
description: La macro DbgLog envía una cadena a la ubicación de salida de depuración, si el registro está habilitado para el tipo y el nivel especificados. Esta macro se omite en las compilaciones comerciales.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Macro DbgLog (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 619a3cd277425b555bc64139c3e59c959cc6abd19d6da22c2129830c38496a24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953344"
---
# <a name="dbglog-macro"></a>Macro DbgLog

La **macro DbgLog** envía una cadena a la ubicación de salida de depuración, si el registro está habilitado para el tipo y el nivel especificados. Esta macro se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
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

Nivel de registro para este mensaje.

</dd> <dt>

*pFormat* 
</dt> <dd>

Cadena **de formato printf-style.**

</dd> <dt>

*...* 
</dt> <dd>

Argumentos adicionales para la cadena de formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve un valor.

## <a name="remarks"></a>Comentarios

Si el registro de depuración de cualquiera de los tipos de mensaje está establecido en el nivel especificado o superior, esta macro envía la cadena con formato a la ubicación de salida de depuración.

La macro agrega automáticamente un carácter de nueva línea a la cadena de salida.

> [!Note]  
> Un conjunto adicional de paréntesis debe incluir los parámetros de macro:

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 




