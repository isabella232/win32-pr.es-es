---
title: Extender funciones de OpenGL
description: La biblioteca de OpenGL admite varias implementaciones de sus funciones.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL en Windows, funciones de extensión
- funciones de extensión OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcbb59aa15a9690ac05728548f0d8073a334a2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994490"
---
# <a name="extending-opengl-functions"></a>Extender funciones de OpenGL

La biblioteca de OpenGL admite varias implementaciones de sus funciones. Las funciones de extensión que se admiten en un contexto de representación no se admiten necesariamente en un contexto de representación diferente. Para un contexto de representación determinado en una aplicación que usa funciones de extensión, use solo las direcciones de función devueltas por la función [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) .

 

 




