---
description: Proporciona al sistema información sobre un documento una vez completada la operación de apertura.
title: Función DlpNotifyPostOpenDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 10121e69ddbdc41516e56ec07e87a2f6dd8148cd
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495892"
---
# <a name="dlpnotifypostopendocument-function"></a>Función DlpNotifyPostOpenDocument

Proporciona al sistema información sobre un documento una vez completada una operación de documento abierto.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*DocumentInfo* \[ En\]
</dt> <dd>

Puntero a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) estructura que contiene información sobre el documento que se abrió.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ En\]
</dt> <dd>

Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la operación de documento abierto.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |