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
# <a name="predefined-mapping-modes"></a><span data-ttu-id="777e9-103">Modos de asignación predefinidos</span><span class="sxs-lookup"><span data-stu-id="777e9-103">Predefined Mapping Modes</span></span>

<span data-ttu-id="777e9-104">De los seis modos de asignación predefinidos, uno depende del dispositivo ( \_ texto mm) y los cinco restantes (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC y mm \_ TWIPS) son independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="777e9-104">Of the six predefined mapping modes, one is device dependent (MM\_TEXT) and the remaining five (MM\_HIENGLISH, MM\_LOENGLISH, MM\_HIMETRIC, MM\_LOMETRIC, and MM\_TWIPS) are device independent.</span></span>

<span data-ttu-id="777e9-105">El modo de asignación predeterminada es \_ texto mm.</span><span class="sxs-lookup"><span data-stu-id="777e9-105">The default mapping mode is MM\_TEXT.</span></span> <span data-ttu-id="777e9-106">Una unidad lógica es igual a un píxel.</span><span class="sxs-lookup"><span data-stu-id="777e9-106">One logical unit equals one pixel.</span></span> <span data-ttu-id="777e9-107">La x positiva es hacia la derecha y la y positiva está inactiva.</span><span class="sxs-lookup"><span data-stu-id="777e9-107">Positive x is to the right, and positive y is down.</span></span> <span data-ttu-id="777e9-108">Este modo se asigna directamente al sistema de coordenadas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="777e9-108">This mode maps directly to the device's coordinate system.</span></span> <span data-ttu-id="777e9-109">La asignación de lógica a física solo implica un desplazamiento en x e y que se define en la ventana controlada por la aplicación y los orígenes de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="777e9-109">The logical-to-physical mapping involves only an offset in x and y that is defined by the application-controlled window and viewport origins.</span></span> <span data-ttu-id="777e9-110">Todas las extensiones de ventanilla y de ventana se establecen en 1, lo que crea una asignación de uno a uno.</span><span class="sxs-lookup"><span data-stu-id="777e9-110">The viewport and window extents are all set to 1, creating a one-to-one mapping.</span></span>

<span data-ttu-id="777e9-111">Las aplicaciones que muestran formas geométricas (círculos, cuadrados, polígonos, etc.) hacen uso de uno de los modos de asignación independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="777e9-111">Applications that display geometric shapes (circles, squares, polygons, and so on) make use of one of the device-independent mapping modes.</span></span> <span data-ttu-id="777e9-112">Por ejemplo, si está escribiendo una aplicación para proporcionar funciones de gráficos para un programa de hoja de cálculo y desea garantizar que el diámetro de cada gráfico circular sea de 2 pulgadas, use el \_ modo de asignación mm LOENGLISH y llame a las funciones adecuadas para dibujar y rellenar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="777e9-112">For example, if you are writing an application to provide charting capabilities for a spreadsheet program and want to guarantee that the diameter of each pie chart is 2 inches, use the MM\_LOENGLISH mapping mode and call the appropriate functions to draw and fill the chart.</span></span> <span data-ttu-id="777e9-113">Especificar MM \_ LOENGLISH garantiza que el diámetro del gráfico sea coherente en cualquier pantalla o impresora.</span><span class="sxs-lookup"><span data-stu-id="777e9-113">Specifying MM\_LOENGLISH, guarantees that the diameter of the chart is consistent on any display or printer.</span></span> <span data-ttu-id="777e9-114">Si \_ se usa texto mm en lugar de mm \_ LOENGLISH, un gráfico que parezca circular en una pantalla VGA aparecerá elíptico en una pantalla de EGA y tendría un aspecto muy pequeño en una impresora láser 300 ppp (puntos por pulgada).</span><span class="sxs-lookup"><span data-stu-id="777e9-114">If MM\_TEXT is used instead of MM\_LOENGLISH, a chart that appears circular on a VGA display would appear elliptical on an EGA display and would appear very small on a 300 dpi (dots per inch) laser printer.</span></span>

 

 



