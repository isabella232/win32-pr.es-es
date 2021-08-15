---
description: Proporciona al sistema información sobre un documento antes de que se inicie una operación de almacenamiento escalonado en el Portapapeles.
title: Función DlpNotifyPreStashClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 920385d9cd57b428ce454415bf1dc57bed7ec4eb1373fa65d42f32668112bb0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976515"
---
# <a name="dlpnotifyprestashclipboard-function"></a>Función DlpNotifyPreStashClipboard

Notifica al sistema antes de que se inicie una operación de almacenamiento escalonado en el Portapapeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyPreStashClipboard();
```



## <a name="parameters"></a>Parámetros




## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |