---
title: Trasladar la función bbox2
description: No hay ningún equivalente de OpenGL para la función bbox2 de la contabilidad de IRIS.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- Migración de la contabilidad de IRIS, función bbox2
- portabilidad de IRIS GL, función bbox2
- portabilidad a OpenGL desde IRIS GL, función bbox2
- Exportación de OpenGL desde IRIS GL, función bbox2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21060b8a11ccd6c44297c8b533bca98d79cc00f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778036"
---
# <a name="porting-the-bbox2-function"></a>Trasladar la función bbox2

No hay ningún equivalente de OpenGL para la función **bbox2** de la contabilidad de iris.

**Para portar código que contiene funciones bbox2**

1.  Cree una nueva lista de visualización (OpenGL) que contenga todo lo que se encuentra en la lista de visualización de la contabilidad de IRIS equivalente, excepto la llamada a **bbox2**.
2.  Use el código de Windows adecuado para dibujar un rectángulo del mismo tamaño que el **BBox** de GL de iris.

 

 




