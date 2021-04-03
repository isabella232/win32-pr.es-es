---
title: ToolBoxBitmap32
description: Identifica el nombre del módulo y el identificador de recurso para un mapa de bits de 16 x 16 que se va a usar para el aspecto de una barra de herramientas o un botón del cuadro de herramientas.
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- Clave del registro ToolBoxBitmap32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ca6208586e961c0b6f8fa666c5731bab38faa6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075544"
---
# <a name="toolboxbitmap32"></a>ToolBoxBitmap32

Identifica el nombre del módulo y el identificador de recurso para un mapa de bits de 16 x 16 que se va a usar para el aspecto de una barra de herramientas o un botón del cuadro de herramientas.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **reg \_ SZ** que especifica el nombre del módulo y el identificador de recurso del mapa de bits.

El tamaño del icono de Windows estándar es demasiado grande para usarse con este fin. Esto requiere que los contenedores de control que tienen un modo de diseño en el que uno selecciona controles y los coloca en un formulario que se está diseñando.

 

 




