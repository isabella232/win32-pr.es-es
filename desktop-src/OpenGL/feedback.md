---
title: Comentarios
description: En el modo de comentarios, cada primitivo que se va a rasterizar genera un bloque de valores que se copia en la matriz de comentarios.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- modo feedback,OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245031"
---
# <a name="feedback-mode"></a>Modo de comentarios

En el modo de comentarios, cada primitivo que se va a rasterizar genera un bloque de valores que se copia en la matriz de comentarios. Proporcione esta matriz [**con glFeedbackBuffer**](glfeedbackbuffer.md), al que debe llamar antes de poner OpenGL en modo de comentarios. Cada bloque de valores comienza con un código que indica el tipo primitivo, seguido de valores que describen los vértices de la primitiva y los datos asociados. Las entradas también se escriben para mapas de bits y rectángulos de píxeles. No se garantiza que los valores se escriban en la matriz de comentarios hasta que llame a [**glRenderMode**](glrendermode.md) para quitar OpenGL del modo de comentarios. Puede usar [**glPassThrough para**](glpassthrough.md) proporcionar un marcador que se devuelve en modo de comentarios como si fuera un primitivo.

 

 




