---
description: Finaliza la configuración de un búfer de seguimiento con campos opcionales para los seguimientos de estilo sprintf.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: SetAsyncTraceParamsEx función)
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
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649683"
---
# <a name="setasynctraceparamsex-function"></a>SetAsyncTraceParamsEx función)

Finaliza la configuración de un búfer de seguimiento con campos opcionales para los seguimientos de estilo **sprintf**.

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

Nombre del módulo que está asociado con el seguimiento.

</dd> <dt>

*pszFile* 
</dt> <dd>

Nombre del archivo de código fuente que contiene la excepción.

</dd> <dt>

*Tarea* 
</dt> <dd>

Número de línea de la excepción en el archivo de código fuente.

</dd> <dt>

*pszFunction* 
</dt> <dd>

Nombre de la función de la excepción.

</dd> <dt>

*dwTraceMask* 
</dt> <dd>

Una constante de marca de seguimiento que representa uno de los tipos de seguimiento disponibles. Este parámetro puede ser cualquiera de los valores siguientes.

<dl> <dt>

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**Irrecuperable \_ \_Máscara de seguimiento** (0x00000001)
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Error \_ de \_Máscara de seguimiento** (0x00000002)
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Depuración \_ \_Máscara de seguimiento** (0x00000004)
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**Estado \_ de \_Máscara de seguimiento** (0x00000008)
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**Inactivo \_ \_Máscara de seguimiento** (0x00000010)
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Mensaje \_ de \_Máscara de seguimiento** (0x00000020)
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Todo \_ \_Máscara de seguimiento** (0xFFFFFFFF)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve 1 si la función se ejecuta correctamente; de lo contrario, devuelve 0.

## <a name="remarks"></a>Observaciones

Exstrace.dll es un componente opcional que se instala con el Protocolo simple de transferencia de correo (SMTP) y el protocolo de transferencia de noticias en red (NNTP).

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
