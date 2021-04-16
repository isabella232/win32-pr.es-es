---
description: La macro DbgLog envía una cadena a la ubicación de salida de depuración, si el registro está habilitado para el tipo y el nivel especificados. Esta macro se omite en las compilaciones comerciales.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Macro DbgLog (Wxdebug. h)
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
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679496"
---
# <a name="dbglog-macro"></a>DbgLog (macro)

La macro **DbgLog** envía una cadena a la ubicación de salida de depuración, si el registro está habilitado para el tipo y el nivel especificados. Esta macro se omite en las compilaciones comerciales.

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

Una cadena de formato de estilo **printf** .

</dd> <dt>

*...* 
</dt> <dd>

Argumentos adicionales para la cadena de formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el registro de depuración para cualquiera de los tipos de mensaje se establece en el nivel especificado o superior, esta macro envía la cadena con formato a la ubicación de salida de depuración.

La macro agrega automáticamente un carácter de nueva línea a la cadena de salida.

> [!Note]  
> Un conjunto adicional de paréntesis debe incluir los parámetros de la macro:

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 




