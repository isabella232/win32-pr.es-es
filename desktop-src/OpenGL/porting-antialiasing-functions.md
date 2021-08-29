---
title: Porting Antialiasing Functions
description: Porting Antialiasing Functions
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- Porte de IRIS GL, suavizado de contorno
- porting from IRIS GL,antialiasing
- porting to OpenGL from IRIS GL,antialiasing
- Porte de OpenGL desde IRIS GL, suavizado de contorno
- suavizado de contorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 130fcf19efd3cd8f1082439bda1bd9c9702c8df7ea41cbe7655828a92e6cc9f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777245"
---
# <a name="porting-antialiasing-functions"></a>Porting Antialiasing Functions

En OpenGL, el modo de subpixel está siempre en on, por lo que el **subpixel** de la función GL de IRIS **(TRUE)** no es necesario y no tiene ningún equivalente openGL. En los temas siguientes se describen aspectos de la porteación de código de suavizado de contorno de IRIS GL.

-   [Porting Blending Code](porting-blending-code.md)
-   [Porting afunction Test Functions](porting-afunction-test-functions.md)
-   [Usar funciones de suavizado de contorno](using-antialiasing-functions.md)

 

 




