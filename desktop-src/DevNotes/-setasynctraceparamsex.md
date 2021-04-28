---
description: 'Función SetAsyncTraceParamsEx: finaliza la configuración de un búfer de seguimiento con campos opcionales para seguimientos de estilo sprintf.'
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: Función SetAsyncTraceParamsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 5a9dc0eee2f4ea3f65fa45914c3340a99ac2d45b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085773"
---
# <a name="setasynctraceparamsex-function"></a>Función SetAsyncTraceParamsEx

Finaliza la configuración de un búfer de seguimiento con campos opcionales para **seguimientos sprintf-style.**

## <a name="syntax"></a>Sintaxis


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszModule* 
</dt> <dd>

Nombre del módulo asociado al seguimiento.

</dd> <dt>

*pszFile* 
</dt> <dd>

Nombre del archivo de origen que contiene la excepción.

</dd> <dt>

*lLine* 
</dt> <dd>

Número de línea de la excepción en el archivo de código fuente.

</dd> <dt>

*pszFunction* 
</dt> <dd>

Nombre de función de la excepción.

</dd> <dt>

*dwTraceMask* 
</dt> <dd>

Constante de marca de seguimiento que representa uno de los tipos de seguimiento disponibles. Este parámetro puede ser cualquiera de los valores siguientes.

<dl> <dt>

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL \_ TRACE \_ MASK** (0x00000001)
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR \_ TRACE \_ MASK** (0x00000002)
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG \_ TRACE \_ MASK** (0x00000004)
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE \_ TRACE \_ MASK** (0x00000008)
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT \_ TRACE \_ MASK** (0x00000010)
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE \_ TRACE \_ MASK** (0x00000020)
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL \_ TRACE \_ MASK** (0xFFFFFFFF)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve 1 si la función se realiza correctamente; de lo contrario, devuelve 0.

## <a name="remarks"></a>Comentarios

Exstrace.dll es un componente opcional que se instala con el Protocolo simple de transferencia de correo (SMTP) y el Protocolo de transferencia de noticias de red (NNTP).

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
