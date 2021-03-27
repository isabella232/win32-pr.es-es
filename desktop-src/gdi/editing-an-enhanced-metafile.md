---
description: Para editar una imagen almacenada en un metarchivo mejorado, una aplicación debe realizar las tareas descritas en el procedimiento siguiente.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Edición de un metarchivo mejorado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155629"
---
# <a name="editing-an-enhanced-metafile"></a><span data-ttu-id="dbf3b-103">Edición de un metarchivo mejorado</span><span class="sxs-lookup"><span data-stu-id="dbf3b-103">Editing an Enhanced Metafile</span></span>

<span data-ttu-id="dbf3b-104">Para editar una imagen almacenada en un metarchivo mejorado, una aplicación debe realizar las tareas descritas en el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-104">To edit a picture stored in an enhanced metafile, an application must perform the tasks described in the following procedure.</span></span>

<span data-ttu-id="dbf3b-105">**Para editar una imagen almacenada en un metarchivo mejorado**</span><span class="sxs-lookup"><span data-stu-id="dbf3b-105">**To edit a picture stored in an enhanced metafile**</span></span>

1.  <span data-ttu-id="dbf3b-106">Use la prueba de posicionamiento para capturar las coordenadas del cursor y recuperar la posición del objeto (línea, arco, rectángulo, elipse, polígono o forma irregular) que el usuario desea modificar.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-106">Use hit-testing to capture the cursor coordinates and retrieve the position of the object (line, arc, rectangle, ellipse, polygon, or irregular shape) that the user wants to alter.</span></span>
2.  <span data-ttu-id="dbf3b-107">Convierta estas coordenadas en unidades lógicas (o universales).</span><span class="sxs-lookup"><span data-stu-id="dbf3b-107">Convert these coordinates to logical (or world) units.</span></span>
3.  <span data-ttu-id="dbf3b-108">Llame a la función [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) y examine cada registro de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-108">Call the [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) function and examine each metafile record.</span></span>
4.  <span data-ttu-id="dbf3b-109">Determinar si un registro determinado corresponde a una función de dibujo de GDI.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-109">Determine whether a given record corresponds to a GDI drawing function.</span></span>
5.  <span data-ttu-id="dbf3b-110">Si es así, determine si las coordenadas almacenadas en el registro se corresponden con la línea, el arco, la elipse o cualquier otro elemento de gráficos que intersecte con las coordenadas especificadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-110">If it does, determine whether the coordinates stored in the record correspond to the line, arc, ellipse, or other graphics element that intersects the coordinates specified by the user.</span></span>
6.  <span data-ttu-id="dbf3b-111">Al buscar el registro que corresponde a la salida que el usuario desea modificar, borre el objeto en la pantalla correspondiente al registro original.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-111">Upon finding the record that corresponds to the output that the user wants to alter, erase the object on the screen that corresponds to the original record.</span></span>
7.  <span data-ttu-id="dbf3b-112">Elimine el registro correspondiente del metarchivo y guarde un puntero en su ubicación.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-112">Delete the corresponding record from the metafile, saving a pointer to its location.</span></span>
8.  <span data-ttu-id="dbf3b-113">Permite al usuario volver a dibujar o reemplazar el objeto.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-113">Permit the user to redraw or replace the object.</span></span>
9.  <span data-ttu-id="dbf3b-114">Convierta las funciones GDI utilizadas para dibujar el nuevo objeto en uno o más registros de metarchivo mejorado.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-114">Convert the GDI functions used to draw the new object into one or more enhanced-metafile records.</span></span>
10. <span data-ttu-id="dbf3b-115">Almacene estos registros en el metarchivo mejorado.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-115">Store these records in the enhanced metafile.</span></span>

 

 



