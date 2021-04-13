---
title: Contextos de representación
description: Un contexto de representación de OpenGL es un puerto a través del cual pasan todos los comandos de OpenGL. Todos los subprocesos que realizan llamadas OpenGL deben tener un contexto de representación actual. Los contextos de representación vinculan OpenGL a los sistemas de ventanas de Windows.
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- OpenGL en Windows, contextos de representación
- contextos de representación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac2ac6c5948da2b7372d600377666cd9e4e074
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357349"
---
# <a name="rendering-contexts"></a>Contextos de representación

Un *contexto de representación* de OpenGL es un puerto a través del cual pasan todos los comandos de OpenGL. Todos los subprocesos que realizan llamadas OpenGL deben tener un contexto de representación actual. Los contextos de representación vinculan OpenGL a los sistemas de ventanas de Windows.

Una aplicación especifica un contexto de dispositivo de Windows cuando crea un contexto de representación. Este contexto de representación es adecuado para dibujar en el dispositivo al que hace referencia el contexto de dispositivo especificado. En concreto, el contexto de representación tiene el mismo formato de píxel que el contexto del dispositivo. Para obtener más información, vea [representar funciones de contexto](rendering-context-functions.md).

A pesar de esta relación, un contexto de representación no es el mismo que un contexto de dispositivo. Un contexto de dispositivo contiene información pertinente para el componente de gráficos (GDI) de Windows. Un contexto de representación contiene información pertinente para OpenGL. Un contexto de dispositivo debe especificarse explícitamente en una llamada GDI. Un contexto de representación está implícito en una llamada de OpenGL. Debe establecer el formato de píxel del contexto del dispositivo antes de crear un contexto de representación.

Un subproceso que realiza llamadas OpenGL debe tener un contexto de representación actual. Si una aplicación realiza llamadas OpenGL desde un subproceso que carece de contexto de representación actual, no sucede nada; la llamada no tiene ningún efecto. Normalmente, una aplicación crea un contexto de representación, lo establece como el contexto de representación actual del subproceso y, a continuación, llama a las funciones de OpenGL. Cuando finaliza la llamada a funciones de OpenGL, la aplicación desacopla el contexto de representación del subproceso y, a continuación, elimina el contexto de representación. Una ventana puede tener varios contextos de representación que se dibujan en ella al mismo tiempo, pero un subproceso solo puede tener un contexto de representación activo actual.

Un contexto de representación actual tiene un contexto de dispositivo asociado. Ese contexto de dispositivo no necesita ser el mismo contexto de dispositivo que el que se usó cuando se creó el contexto de representación, pero debe hacer referencia al mismo dispositivo y tener el mismo formato de píxeles.

Un subproceso solo puede tener un contexto de representación actual. Un contexto de representación puede ser actual a un solo subproceso.

 

 




