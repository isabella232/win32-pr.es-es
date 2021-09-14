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
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069302"
---
# <a name="porting-antialiasing-functions"></a>Porting Antialiasing Functions

En OpenGL, el modo de subpíxel está siempre on, por lo que el **subpíxel** de función GL de IRIS **(TRUE)** no es necesario y no tiene ningún equivalente openGL. En los temas siguientes se describen aspectos de la porte del código de suavizado de contorno de IRIS GL.

-   [Porting Blending Code](porting-blending-code.md)
-   [Porte de funciones de prueba afunction](porting-afunction-test-functions.md)
-   [Uso de funciones de suavizado de contorno](using-antialiasing-functions.md)

 

 




