---
description: Determina si la aplicación debe extraer los datos del Portapapeles del sistema en lugar de tomarlo de su caché interna.
title: Función DlpMustPasteFromSystemClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e111cb85c6eada6f84f7bc10eb240e89447a173e741b26b316b232d742f8de48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888585"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a>Función DlpMustPasteFromSystemClipboard

Determina si la aplicación debe extraer los datos del Portapapeles del sistema en lugar de tomarlo de su caché interna.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a>Valor devuelto

TRUE si es obligatorio llamar al Portapapeles del sistema operativo; de lo contrario, FALSE.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |