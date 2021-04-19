---
description: Proporciona al sistema información sobre un documento cuando se introduce un destino de colocación.
title: Función DlpNotifyEnterDropTarget (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyEnterDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: ec1eee1cee7bbcc38ce3094e3e2f8b650cf3b2a9
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495901"
---
# <a name="dlpnotifyenterdroptarget-function"></a>Función DlpNotifyEnterDropTarget

Proporciona al sistema información sobre un documento cuando se introduce un destino de colocación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DocumentInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento asociado a la operación de colocación.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |