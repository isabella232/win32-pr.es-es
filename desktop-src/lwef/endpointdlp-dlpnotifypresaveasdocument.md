---
description: Proporciona al sistema información sobre un documento antes de iniciar una operación de guardar como.
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
ms.openlocfilehash: 5226ed63227e2d9dd01155066e2e6e19f77e063f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495820"
---
# <a name="dlpnotifypresaveasdocument-function"></a>Función DlpNotifyPreSaveAsDocument

Proporciona al sistema información sobre un documento antes de iniciar una operación de guardar como.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DocumentInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento que se va a guardar.

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