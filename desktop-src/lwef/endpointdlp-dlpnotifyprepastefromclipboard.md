---
description: Proporciona al sistema información sobre un documento antes de iniciar una operación de pegar desde el Portapapeles.
title: Función DlpNotifyPrePasteFromClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cfec6e7abbf2b94ce8bf78e0b1a10082ec54419d
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495815"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a>Función DlpNotifyPrePasteFromClipboard

Proporciona al sistema información sobre un documento antes de iniciar una operación de pegar desde el Portapapeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DocumentInfo* \[ En\]
</dt> <dd>

Puntero a una [estructura PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento en el que se pega el contenido.

</dd> </dl>




## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |