---
title: Modo retenido frente al modo inmediato
description: Las API de gráficos pueden dividirse en API de modo retenido y API de modo inmediato.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104562158"
---
# <a name="retained-mode-versus-immediate-mode"></a>Modo retenido frente al modo inmediato

Las API de gráficos pueden dividirse en API de *modo retenido* y API *de modo inmediato* . Direct2D es una API de modo inmediato. Windows Presentation Foundation (WPF) es un ejemplo de una API de modo retenido.

Una API de modo retenido es declarativo. La aplicación crea una escena a partir de primitivas de gráficos, como formas y líneas. La biblioteca de gráficos almacena un modelo de la escena en la memoria. Para dibujar un marco, la biblioteca de gráficos transforma la escena en un conjunto de comandos de dibujo. Entre fotogramas, la biblioteca de gráficos mantiene la escena en memoria. Para cambiar lo que se representa, la aplicación emite un comando para actualizar la escena, por ejemplo, para agregar o quitar una forma. A continuación, la biblioteca es responsable de volver a dibujar la escena.

![diagrama que muestra los gráficos en modo retenido.](images/graphics06.png)

Una API de modo inmediato es un procedimiento. Cada vez que se dibuja un nuevo fotograma, la aplicación emite directamente los comandos de dibujo. La biblioteca de gráficos no almacena un modelo de escena entre fotogramas. En su lugar, la aplicación realiza un seguimiento de la escena.

![diagrama que muestra los gráficos en modo inmediato.](images/graphics07.png)

Las API de modo retenido pueden ser más fáciles de usar, ya que la API hace más trabajo para usted, como la inicialización, el mantenimiento del estado y la limpieza. Por otro lado, suelen ser menos flexibles, ya que la API impone su propio modelo de escena. Además, una API de modo retenido puede tener más requisitos de memoria, ya que debe proporcionar un modelo de escena de uso general. Con una API de modo inmediato, puede implementar optimizaciones de destino.

## <a name="next"></a>Siguientes

[Su primer programa de Direct2D](your-first-direct2d-program.md)

 

 




