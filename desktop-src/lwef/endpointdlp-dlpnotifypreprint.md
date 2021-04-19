---
description: Proporciona al sistema información sobre un documento antes de iniciar una operación de impresión.
title: Función DlpNotifyPrePrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: eef5e3a19a6b93a49ba8b600be77385a99d3153a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495819"
---
# <a name="dlpnotifypreprint-function"></a>Función DlpNotifyPrePrint

Proporciona al sistema información sobre un documento antes de iniciar una operación de impresión.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DocumentInfo* \[ En\]
</dt> <dd>

Puntero a una [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) estructura que contiene información sobre el documento que se va a imprimir.

</dd> </dl>

<dl> <dt>

*PrintInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) que contiene información sobre la operación de impresión.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |