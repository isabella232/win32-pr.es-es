---
description: 'Función AsyncStringTrace: finaliza la configuración de un búfer de seguimiento con campos opcionales para seguimientos de estilo sprintf.'
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: Función AsyncStringTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: ac099b0b69c1417c428aefe04b8e6591f945545a2b69196da588ebce8de23f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076179"
---
# <a name="asyncstringtrace-function"></a>Función AsyncStringTrace

Finaliza la configuración de un búfer de seguimiento con campos opcionales para **seguimientos sprintf-style.**

## <a name="syntax"></a>Sintaxis


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Parámetro de seguimiento de 32 bits que se usa para el filtrado en el nivel de aplicación.

</dd> <dt>

*szFormat* 
</dt> <dd>

Cadena terminada en cero que describe el formato del seguimiento.

</dd> <dt>

*Marcador* 
</dt> <dd>

Marcador para las **funciones vsprintf.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve la longitud de la instrucción de seguimiento, en bytes.

## <a name="remarks"></a>Comentarios

Exstrace.dll es un componente opcional que se instala con el Protocolo simple de transferencia de correo (SMTP) y el Protocolo de transferencia de noticias de red (NNTP).

El **tipo de datos va \_ list** es un tipo estándar que se usa para contener la información necesaria para las **macros va \_ arg** y **va \_ end.** Para obtener más información, vea [Tipos estándar.](/cpp/c-runtime-library/standard-types?view=vs-2019)

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

