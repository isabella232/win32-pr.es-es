---
description: De los seis modos de asignación predefinidos, uno depende del dispositivo ( \_ texto mm) y los cinco restantes (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC y mm \_ TWIPS) son independientes del dispositivo.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Modos de asignación predefinidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984851"
---
# <a name="predefined-mapping-modes"></a>Modos de asignación predefinidos

De los seis modos de asignación predefinidos, uno depende del dispositivo ( \_ texto mm) y los cinco restantes (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC y mm \_ TWIPS) son independientes del dispositivo.

El modo de asignación predeterminada es \_ texto mm. Una unidad lógica es igual a un píxel. La x positiva es hacia la derecha y la y positiva está inactiva. Este modo se asigna directamente al sistema de coordenadas del dispositivo. La asignación de lógica a física solo implica un desplazamiento en x e y que se define en la ventana controlada por la aplicación y los orígenes de la ventanilla. Todas las extensiones de ventanilla y de ventana se establecen en 1, lo que crea una asignación de uno a uno.

Las aplicaciones que muestran formas geométricas (círculos, cuadrados, polígonos, etc.) hacen uso de uno de los modos de asignación independientes del dispositivo. Por ejemplo, si está escribiendo una aplicación para proporcionar funciones de gráficos para un programa de hoja de cálculo y desea garantizar que el diámetro de cada gráfico circular sea de 2 pulgadas, use el \_ modo de asignación mm LOENGLISH y llame a las funciones adecuadas para dibujar y rellenar el gráfico. Especificar MM \_ LOENGLISH garantiza que el diámetro del gráfico sea coherente en cualquier pantalla o impresora. Si \_ se usa texto mm en lugar de mm \_ LOENGLISH, un gráfico que parezca circular en una pantalla VGA aparecerá elíptico en una pantalla de EGA y tendría un aspecto muy pequeño en una impresora láser 300 ppp (puntos por pulgada).

 

 



