---
description: Una paleta de colores es una matriz que contiene valores de color que identifican los colores que se pueden mostrar o dibujar actualmente en el dispositivo de salida.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Paletas de colores (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155657"
---
# <a name="color-palettes-windows-gdi"></a><span data-ttu-id="a772e-103">Paletas de colores (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="a772e-103">Color Palettes (Windows GDI)</span></span>

<span data-ttu-id="a772e-104">Una paleta de colores es una matriz que contiene valores de color que identifican los colores que se pueden mostrar o dibujar actualmente en el dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="a772e-104">A color palette is an array that contains color values identifying the colors that can currently be displayed or drawn on the output device.</span></span> <span data-ttu-id="a772e-105">Las paletas de colores las utilizan los dispositivos que son capaces de generar muchos colores, pero que solo pueden mostrar o dibujar un subconjunto de ellos en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="a772e-105">Color palettes are used by devices that are capable of generating many colors but that can only display or draw a subset of these at any given time.</span></span> <span data-ttu-id="a772e-106">Para estos dispositivos, el sistema mantiene una *paleta del sistema* para realizar un seguimiento de los colores actuales del dispositivo y administrarlos.</span><span class="sxs-lookup"><span data-stu-id="a772e-106">For such devices, the system maintains a *system palette* to track and manage the current colors of the device.</span></span> <span data-ttu-id="a772e-107">Las aplicaciones no tienen acceso directo a la paleta del sistema.</span><span class="sxs-lookup"><span data-stu-id="a772e-107">Applications do not have direct access to the system palette.</span></span> <span data-ttu-id="a772e-108">En su lugar, el sistema asocia una paleta predeterminada con cada contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a772e-108">Instead, the system associates a default palette with each device context.</span></span> <span data-ttu-id="a772e-109">Las aplicaciones pueden usar los colores de la paleta predeterminada o definir sus propios colores creando *paletas lógicas* y asociándolos con contextos de dispositivo individuales.</span><span class="sxs-lookup"><span data-stu-id="a772e-109">Applications can use the colors in the default palette or define their own colors by creating *logical palettes* and associating them with individual device contexts.</span></span>

<span data-ttu-id="a772e-110">Una aplicación puede determinar si un dispositivo admite las paletas de colores comprobando el \_ bit de la paleta RC en el valor RASTERCAPS devuelto por la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="a772e-110">An application can determine whether a device supports color palettes by checking for the RC\_PALETTE bit in the RASTERCAPS value returned by the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function.</span></span>

 

 



