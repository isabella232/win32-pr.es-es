---
title: Prueba de estarcido
description: La prueba de la galería de símbolos descarta condicionalmente un fragmento según el resultado de una comparación entre el valor del búfer de estarcido y un valor de referencia.
ms.assetid: 967be1e5-a9a2-45cc-aae7-c33cc257ade1
keywords:
- Canalización de procesamiento de OpenGL, prueba de estarcido
- Galería de símbolos de prueba OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e285c3dfb1591c5ed3d95969024d2350a7517a79
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779465"
---
# <a name="stencil-test"></a>Prueba de estarcido

La prueba de la galería de símbolos descarta condicionalmente un fragmento según el resultado de una comparación entre el valor del búfer de estarcido y un valor de referencia. La función [**glStencilFunc**](glstencilfunc.md) especifica la función de comparación y el valor de referencia. Si el fragmento supera o no la prueba de estarcido, el valor del búfer de estarcido se modifica según las instrucciones especificadas con [**glStencilOp**](glstencilop.md).

 

 




