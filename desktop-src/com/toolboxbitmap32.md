---
title: ToolBoxBitmap32
description: Identifica el nombre del módulo y el identificador de recurso de un mapa de bits de 16 x 16 que se usará para la cara de una barra de herramientas o un botón del cuadro de herramientas.
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- ToolBoxBitmap32 clave del Registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ca6208586e961c0b6f8fa666c5731bab38faa6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369600"
---
# <a name="toolboxbitmap32"></a>ToolBoxBitmap32

Identifica el nombre del módulo y el identificador de recurso de un mapa de bits de 16 x 16 que se usará para la cara de una barra de herramientas o un botón del cuadro de herramientas.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a>Observaciones

Se trata de un **valor \_ SZ reg** que especifica el nombre del módulo y el identificador de recursos para el mapa de bits.

El tamaño Windows icono de imagen estándar es demasiado grande para usarse para este propósito. Esto requiere contenedores de controles que tienen un modo de diseño en el que se seleccionan los controles y se coloca en un formulario que se está diseñando.

 

 




