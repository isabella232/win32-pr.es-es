---
description: Proporciona al sistema información de estado una vez completada una operación de almacenamiento escalonado del Portapapeles.
title: Función DlpNotifyPostStashClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 97366a356b960fb8bea87bf552bf98576363663a6ca21de290d4035414fcb904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751664"
---
# <a name="dlpnotifypoststashclipboard-function"></a>Función DlpNotifyPostStashClipboard

Proporciona al sistema información de estado una vez completada una operación de almacenamiento escalonado del Portapapeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parámetros


<dl> <dt>

*OpStatus* \[ En\]
</dt> <dd>

Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la operación de stash del Portapapeles.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |