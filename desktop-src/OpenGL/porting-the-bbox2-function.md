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
ms.openlocfilehash: 21060b8a11ccd6c44297c8b533bca98d79cc00f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362042"
---
# <a name="porting-the-bbox2-function"></a>Porte de la función bbox2

No hay ningún equivalente openGL para la función **bbox2** iris GL.

**Para porte el código que contiene funciones bbox2**

1.  Cree una nueva lista de visualización (OpenGL) que contenga todo el contenido de la lista de visualización de IRIS GL equivalente, excepto la llamada **a bbox2**.
2.  Use el código Windows para dibujar un rectángulo del mismo tamaño que el **cuadro bbox** IRIS GL .

 

 




