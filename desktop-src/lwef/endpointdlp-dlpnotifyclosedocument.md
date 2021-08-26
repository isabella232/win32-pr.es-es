---
description: Proporciona al sistema información sobre un documento antes de iniciar la operación de cierre del documento.
title: Función DlpNotifyCloseDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: f8818e55482420c6b1fd307392138b99d391f4df9b703477ce4c3e950b36f4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962785"
---
# <a name="dlpnotifyclosedocument-function"></a>Función DlpNotifyCloseDocument

Proporciona al sistema información sobre un documento antes de iniciar la operación de cierre del documento.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DocumentInfo* \[ En\]
</dt> <dd>

Puntero a [un](endpointdlp-dlp_document_info.md) PDLP_DOCUMENT_INFO estructura que contiene información sobre el documento que se va a abrir.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |