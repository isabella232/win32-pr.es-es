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
# <a name="toolboxbitmap32"></a><span data-ttu-id="4403f-104">ToolBoxBitmap32</span><span class="sxs-lookup"><span data-stu-id="4403f-104">ToolBoxBitmap32</span></span>

<span data-ttu-id="4403f-105">Identifica el nombre del módulo y el identificador de recurso para un mapa de bits de 16 x 16 que se va a usar para el aspecto de una barra de herramientas o un botón del cuadro de herramientas.</span><span class="sxs-lookup"><span data-stu-id="4403f-105">Identifies the module name and resource ID for a 16 x 16 bitmap to use for the face of a toolbar or toolbox button.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4403f-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="4403f-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a><span data-ttu-id="4403f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4403f-107">Remarks</span></span>

<span data-ttu-id="4403f-108">Se trata de un valor de **reg \_ SZ** que especifica el nombre del módulo y el identificador de recurso del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="4403f-108">This is a **REG\_SZ** value that specifies the module name and resource identifier for the bitmap.</span></span>

<span data-ttu-id="4403f-109">El tamaño del icono de Windows estándar es demasiado grande para usarse con este fin.</span><span class="sxs-lookup"><span data-stu-id="4403f-109">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="4403f-110">Esto requiere que los contenedores de control que tienen un modo de diseño en el que uno selecciona controles y los coloca en un formulario que se está diseñando.</span><span class="sxs-lookup"><span data-stu-id="4403f-110">This requires control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span>

 

 




