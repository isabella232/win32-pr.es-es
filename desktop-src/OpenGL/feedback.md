---
title: Comentarios
description: En el modo de comentarios, cada primitiva que se va a rasterizar genera un bloque de valores que se copia en la matriz de comentarios.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- modo de comentarios, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678652"
---
# <a name="feedback-mode"></a>Modo de comentarios

En el modo de comentarios, cada primitiva que se va a rasterizar genera un bloque de valores que se copia en la matriz de comentarios. Suministre esta matriz con [**glFeedbackBuffer**](glfeedbackbuffer.md), que debe llamar antes de colocar OpenGL en modo de comentarios. Cada bloque de valores comienza con un código que indica el tipo primitivo, seguido de los valores que describen los vértices del primitivo y los datos asociados. Las entradas también se escriben para los mapas de bits y los rectángulos de píxeles. No se garantiza que los valores se escriban en la matriz de comentarios hasta que llame a [**glRenderMode**](glrendermode.md) para sacar el modo de comentarios de OpenGL. Puede usar [**glPassThrough**](glpassthrough.md) para proporcionar un marcador que se devuelve en modo de comentarios como si fuera un primitivo.

 

 




