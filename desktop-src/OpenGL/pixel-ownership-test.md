---
title: Prueba de propiedad de píxeles
description: La prueba de propiedad de píxeles determina si el contexto de OpenGL actual posee el píxel en el fotogramas correspondiente a un fragmento determinado.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Canalización de procesamiento de OpenGL, prueba de propiedad de píxeles
- prueba de propiedad de píxeles OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357251"
---
# <a name="pixel-ownership-test"></a>Prueba de propiedad de píxeles

La prueba de propiedad de píxeles determina si el contexto de OpenGL actual posee el píxel en el fotogramas correspondiente a un fragmento determinado. Si es así, el fragmento continúa con la siguiente prueba. De lo contrario, el sistema de ventanas determina si el fragmento se descarta o si se realizarán más operaciones de fragmento con ese fragmento. Con esta prueba, el sistema de ventanas controla el comportamiento cuando, por ejemplo, se oculta una ventana de OpenGL.

 

 




