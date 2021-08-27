---
description: Proporciona al sistema información sobre un documento una vez completada una operación de arrastrar y colocar.
title: Función DlpNotifyPostDragDrop (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 3d20f9356007973b580d136aef1a74b8206026bf62fe14c5db46eb2cc0cbf1f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062115"
---
# <a name="dlpnotifypostdragdrop-function"></a>Función DlpNotifyPostDragDrop

Proporciona al sistema información sobre un documento una vez completada una operación de arrastrar y colocar.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DocumentInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento asociado a la operación de arrastrar y colocar.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ En\]
</dt> <dd>

Puntero a una estructura [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contiene información de estado sobre la colocación de arrastre.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |