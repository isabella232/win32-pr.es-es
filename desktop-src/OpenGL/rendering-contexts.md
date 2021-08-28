---
title: Representación de contextos
description: Un contexto de representación de OpenGL es un puerto por el que pasan todos los comandos de OpenGL. Cada subproceso que realiza llamadas OpenGL debe tener un contexto de representación actual. Los contextos de representación vinculan OpenGL a los Windows ventanas.
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- OpenGL en Windows, contextos de representación
- contextos de representación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51167161662501f8aaaca6a392b2efc84217be139842c343056746abf0c35161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011953"
---
# <a name="rendering-contexts"></a>Representación de contextos

Un contexto de *representación de* OpenGL es un puerto por el que pasan todos los comandos de OpenGL. Cada subproceso que realiza llamadas OpenGL debe tener un contexto de representación actual. Los contextos de representación vinculan OpenGL a los Windows ventanas.

Una aplicación especifica un Windows de dispositivo cuando crea un contexto de representación. Este contexto de representación es adecuado para dibujar en el dispositivo al que hace referencia el contexto de dispositivo especificado. En concreto, el contexto de representación tiene el mismo formato de píxel que el contexto del dispositivo. Para obtener más información, vea [Representación de funciones de contexto](rendering-context-functions.md).

A pesar de esta relación, un contexto de representación no es el mismo que un contexto de dispositivo. Un contexto de dispositivo contiene información pertinente para el componente de gráficos (GDI) de Windows. Un contexto de representación contiene información pertinente para OpenGL. Un contexto de dispositivo debe especificarse explícitamente en una llamada GDI. Un contexto de representación es implícito en una llamada OpenGL. Debe establecer el formato de píxel de un contexto de dispositivo antes de crear un contexto de representación.

Un subproceso que realiza llamadas OpenGL debe tener un contexto de representación actual. Si una aplicación realiza llamadas OpenGL desde un subproceso que carece de un contexto de representación actual, no ocurre nada; la llamada no tiene ningún efecto. Normalmente, una aplicación crea un contexto de representación, lo establece como contexto de representación actual de un subproceso y, a continuación, llama a las funciones OpenGL. Cuando termina de llamar a funciones openGL, la aplicación desacopla el contexto de representación del subproceso y, a continuación, elimina el contexto de representación. Una ventana puede tener varios contextos de representación dibujados a la vez, pero un subproceso solo puede tener un contexto de representación activo actual.

Un contexto de representación actual tiene un contexto de dispositivo asociado. Ese contexto de dispositivo no debe ser el mismo que el que se usó cuando se creó el contexto de representación, pero debe hacer referencia al mismo dispositivo y tener el mismo formato de píxel.

Un subproceso solo puede tener un contexto de representación actual. Un contexto de representación solo puede ser actual en un subproceso.

 

 




