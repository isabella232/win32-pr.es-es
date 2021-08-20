---
title: Porte de la función bbox2
description: No hay ningún equivalente openGL para la función bbox2 iris GL.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- Porte de IRIS GL, función bbox2
- porting from IRIS GL,bbox2 function
- porting to OpenGL from IRIS GL,bbox2 function
- Porte de OpenGL desde IRIS GL, función bbox2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f34bc9035e9aa9fac884a14946a0593cb70702cf19f22d5d4c82011b58077e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012013"
---
# <a name="porting-the-bbox2-function"></a>Porte de la función bbox2

No hay ningún equivalente openGL para la función **bbox2** iris GL.

**Para porte el código que contiene funciones bbox2**

1.  Cree una nueva lista de visualización (OpenGL) que contenga todo el contenido de la lista de visualización de IRIS GL equivalente, excepto la llamada **a bbox2**.
2.  Use el código Windows para dibujar un rectángulo del mismo tamaño que el **bbox** IRIS GL .

 

 




