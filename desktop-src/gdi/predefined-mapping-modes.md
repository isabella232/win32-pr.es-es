---
description: De los seis modos de asignación predefinidos, uno depende del dispositivo (MM TEXT) y los cinco \_ restantes (MM \_ HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM LOMETRIC y \_ MM \_ TWIPS) son independientes del dispositivo.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Modos de asignación predefinidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c0eecce6196672db11d61326c82364c1fde1d1b494e48ff77e214e79df91e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037683"
---
# <a name="predefined-mapping-modes"></a>Modos de asignación predefinidos

De los seis modos de asignación predefinidos, uno depende del dispositivo (MM TEXT) y los cinco \_ restantes (MM \_ HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM LOMETRIC y \_ MM \_ TWIPS) son independientes del dispositivo.

El modo de asignación predeterminado es MM \_ TEXT. Una unidad lógica es igual a un píxel. La x positiva está a la derecha y la y positiva está abajo. Este modo se asigna directamente al sistema de coordenadas del dispositivo. La asignación de lógica a física implica solo un desplazamiento en x e y definido por los orígenes de ventana y ventanilla controlados por la aplicación. Las extensiones de ventanilla y ventana se establecen en 1, lo que crea una asignación uno a uno.

Las aplicaciones que muestran formas geométricas (círculos, cuadrados, polígonos, entre otros) usan uno de los modos de asignación independientes del dispositivo. Por ejemplo, si está escribiendo una aplicación para proporcionar funcionalidades de gráficos para un programa de hoja de cálculo y desea garantizar que el grosor de cada gráfico circular es de 2 pulgadas, use el modo de asignación MM LOENGLISH y llame a las funciones adecuadas para dibujar y rellenar el \_ gráfico. Al especificar MM LOENGLISH, se garantiza que el grosor del gráfico sea \_ coherente en cualquier pantalla o impresora. Si se usa MM TEXT en lugar de MM LOENGLISH, un gráfico que aparece circular en una pantalla VGA aparecería elíptico en una pantalla EGA y sería muy pequeño en una impresora de \_ \_ 300 ppp (puntos por pulgada).

 

 



