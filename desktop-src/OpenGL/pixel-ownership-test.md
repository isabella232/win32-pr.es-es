---
title: Prueba de propiedad de píxeles
description: La prueba de propiedad de píxeles determina si el contexto openGL actual posee el píxel del búfer de fotogramas correspondiente a un fragmento determinado.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Canalización de procesamiento de OpenGL, prueba de propiedad de píxeles
- Prueba de propiedad de píxeles OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171341"
---
# <a name="pixel-ownership-test"></a>Prueba de propiedad de píxeles

La prueba de propiedad de píxeles determina si el contexto openGL actual posee el píxel del búfer de fotogramas correspondiente a un fragmento determinado. Si es así, el fragmento pasa a la siguiente prueba. Si no es así, el sistema de ventanas determina si el fragmento se descarta o si se realizarán más operaciones de fragmento con ese fragmento. Con esta prueba, el sistema de ventanas controla el comportamiento cuando, por ejemplo, se oculta una ventana OpenGL.

 

 




