---
description: Proporciona al sistema información sobre un documento antes de iniciar una operación guardar como.
title: Función DlpNotifyPreSaveAsDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 1dbd565ac7a86e381e1e70facf79a2883182260f82c31a2e8a9a3de4f6da8f2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778225"
---
# <a name="dlpnotifypresaveasdocument-function"></a>Función DlpNotifyPreSaveAsDocument

Proporciona al sistema información sobre un documento antes de iniciar una operación guardar como.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DocumentInfo* \[ En\]
</dt> <dd>

Puntero a una [estructura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento que se va a guardar.

</dd> </dl>

<dl> <dt>

*Destino* \[ En\]
</dt> <dd>

**LPCWSTR que** contiene la ruta de acceso de destino del documento que se va a guardar.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |