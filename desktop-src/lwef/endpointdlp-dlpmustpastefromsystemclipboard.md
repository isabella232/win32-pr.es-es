---
description: Determina si la aplicación debe extraer los datos del Portapapeles del sistema en lugar de tomar los datos de su caché interna.
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
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495916"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a>Función DlpMustPasteFromSystemClipboard

Determina si la aplicación debe extraer los datos del Portapapeles del sistema en lugar de tomar los datos de su caché interna.

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