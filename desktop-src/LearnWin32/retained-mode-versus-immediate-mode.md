---
title: Modo retenido frente al modo inmediato
description: Las API de gráficos se pueden dividir en API de modo retenido y API de modo inmediato.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159937"
---
# <a name="retained-mode-versus-immediate-mode"></a>Modo retenido frente al modo inmediato

Las API de gráficos se pueden dividir en API *de modo retenido* y API *de modo* inmediato. Direct2D es una API en modo inmediato. Windows Presentation Foundation (WPF) es un ejemplo de una API en modo retenido.

Una API en modo retenido es declarativa. La aplicación construye una escena a partir de primitivas gráficas, como formas y líneas. La biblioteca de gráficos almacena un modelo de la escena en memoria. Para dibujar un marco, la biblioteca de gráficos transforma la escena en un conjunto de comandos de dibujo. Entre fotogramas, la biblioteca de gráficos mantiene la escena en memoria. Para cambiar lo que se representa, la aplicación emite un comando para actualizar la escena, por ejemplo, para agregar o quitar una forma. A continuación, la biblioteca es responsable de volver a dibujar la escena.

![diagrama que muestra gráficos en modo retenido.](images/graphics06.png)

Una API en modo inmediato es un procedimiento. Cada vez que se dibuja un nuevo marco, la aplicación emite directamente los comandos de dibujo. La biblioteca de gráficos no almacena un modelo de escena entre fotogramas. En su lugar, la aplicación realiza un seguimiento de la escena.

![diagrama que muestra gráficos en modo inmediato.](images/graphics07.png)

Las API en modo retenido pueden ser más sencillas de usar, ya que la API realiza más de su trabajo, como la inicialización, el mantenimiento del estado y la limpieza. Por otro lado, a menudo son menos flexibles, porque la API impone su propio modelo de escena. Además, una API en modo retenido puede tener requisitos de memoria mayores, ya que debe proporcionar un modelo de escena de uso general. Con una API en modo inmediato, puede implementar optimizaciones de destino.

## <a name="next"></a>Siguientes

[Su primer programa de Direct2D](your-first-direct2d-program.md)

 

 




