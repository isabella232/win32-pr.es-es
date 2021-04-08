---
title: Windows (conceptos básicos del diseño)
description: Windows son los principales \ 0034; canvass \ 0034; o superficies de la interfaz de usuario de la aplicación de escritorio, incluidas las ventanas principales y los elementos emergentes, cuadros de diálogo y asistentes. Siga estas instrucciones a la hora de decidir qué superficie usar y cuál es la mejor manera de usarlas.
ms.assetid: E1FA78DA-D580-4B0E-AB59-29F013278766
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5b7bb58750635af25d49208992d5583c44520a04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003289"
---
# <a name="windows-design-basics"></a><span data-ttu-id="84e30-104">Windows (conceptos básicos del diseño)</span><span class="sxs-lookup"><span data-stu-id="84e30-104">Windows (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="84e30-105">Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="84e30-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="84e30-106">Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="84e30-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="84e30-107">Windows son las principales "lienzos" o superficies de interfaz de usuario de la aplicación de escritorio, incluidas las ventanas principales y los elementos emergentes, cuadros de diálogo y asistentes.</span><span class="sxs-lookup"><span data-stu-id="84e30-107">Windows are the main "canvases" or UI surfaces of your desktop app, including the main windows itself and pop-ups, dialogs, and wizards.</span></span> <span data-ttu-id="84e30-108">Siga estas instrucciones a la hora de decidir qué superficie usar y cuál es la mejor manera de usarlas.</span><span class="sxs-lookup"><span data-stu-id="84e30-108">Follow these guidelines when deciding which surface to use and how best to use them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="84e30-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="84e30-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84e30-110">Tema</span><span class="sxs-lookup"><span data-stu-id="84e30-110">Topic</span></span></th>
<th><span data-ttu-id="84e30-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="84e30-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84e30-112"><a href="win-window-mgt.md">Administración de ventanas</a></span><span class="sxs-lookup"><span data-stu-id="84e30-112"><a href="win-window-mgt.md">Window Management</a></span></span><br/></td>
<td><span data-ttu-id="84e30-113">En este artículo se trata la ubicación predeterminada de las ventanas cuando se muestran inicialmente en la pantalla, el orden de apilamiento con respecto a otras ventanas (<a href="glossary.md">orden Z</a>), su tamaño inicial y el modo en que su pantalla afecta al foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="84e30-113">This article covers default placement of windows when initially displayed on the screen, their stacking order relative to other windows (<a href="glossary.md">Z order</a>), their initial size, and how their display affects input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84e30-114"><a href="win-window-frames.md">Marcos de ventana</a></span><span class="sxs-lookup"><span data-stu-id="84e30-114"><a href="win-window-frames.md">Window Frames</a></span></span><br/></td>
<td><span data-ttu-id="84e30-115">La mayoría de los programas deben usar marcos de ventana estándar.</span><span class="sxs-lookup"><span data-stu-id="84e30-115">Most programs should use standard window frames.</span></span> <span data-ttu-id="84e30-116">Las aplicaciones envolventes pueden tener un modo de pantalla completa que oculte el marco de la ventana.</span><span class="sxs-lookup"><span data-stu-id="84e30-116">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="84e30-117">Considere la posibilidad de usar cristal estratégicamente para obtener un aspecto más sencillo, más claro y más coherente.</span><span class="sxs-lookup"><span data-stu-id="84e30-117">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84e30-118"><a href="win-dialog-box.md">Cuadros de diálogo</a></span><span class="sxs-lookup"><span data-stu-id="84e30-118"><a href="win-dialog-box.md">Dialog Boxes</a></span></span><br/></td>
<td><span data-ttu-id="84e30-119">Un cuadro de diálogo es una ventana secundaria que permite a los usuarios realizar un comando, preguntar a los usuarios o proporcionar información sobre el progreso o los usuarios.</span><span class="sxs-lookup"><span data-stu-id="84e30-119">A dialog box is a secondary window that allows users to perform a command, asks users a question, or provides users with information or progress feedback.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84e30-120"><a href="win-common-dlg.md">Cuadros de diálogo comunes</a></span><span class="sxs-lookup"><span data-stu-id="84e30-120"><a href="win-common-dlg.md">Common Dialogs</a></span></span><br/></td>
<td><span data-ttu-id="84e30-121">Los cuadros de diálogo comunes de Microsoft Windows se componen de los cuadros de diálogo Abrir archivo, guardar archivo, abrir carpeta, buscar y reemplazar, imprimir, configurar página, fuente y color.</span><span class="sxs-lookup"><span data-stu-id="84e30-121">The Microsoft Windows common dialogs consist of the Open File, Save File, Open Folder, Find and Replace, Print, Page Setup, Font, and Color dialog boxes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84e30-122"><a href="win-wizards.md">Asistentes</a></span><span class="sxs-lookup"><span data-stu-id="84e30-122"><a href="win-wizards.md">Wizards</a></span></span><br/></td>
<td><span data-ttu-id="84e30-123">A pesar de que es maravilloso, el nombre de divertidos, los asistentes no son una forma especial de interfaz de usuario y solo tienen un determinado intervalo de utilidad.</span><span class="sxs-lookup"><span data-stu-id="84e30-123">Despite that wonderful, whimsical name, wizards are not really a special form of user interface, and they have only a particular range of utility.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84e30-124"><a href="win-property-win.md">Ventanas de propiedades</a></span><span class="sxs-lookup"><span data-stu-id="84e30-124"><a href="win-property-win.md">Property Windows</a></span></span><br/></td>
<td><span data-ttu-id="84e30-125">La ventana de propiedades es el nombre colectivo para los siguientes tipos de interfaces de usuario (IU):</span><span class="sxs-lookup"><span data-stu-id="84e30-125">Property window is the collective name for the following types of user interfaces (UIs):</span></span><br/>
<ul>
<li><span data-ttu-id="84e30-126">Hoja de propiedades: se usa para <strong>ver y cambiar las propiedades de un objeto o una colección de objetos en un cuadro de diálogo</strong>.</span><span class="sxs-lookup"><span data-stu-id="84e30-126">Property sheet: used to <strong>view and change properties for an object or collection of objects in a dialog box</strong>.</span></span></li>
<li><span data-ttu-id="84e30-127">Inspector de propiedad: se usa para <strong>ver y cambiar las propiedades de un objeto o una colección de objetos en un panel</strong>.</span><span class="sxs-lookup"><span data-stu-id="84e30-127">Property inspector: used to <strong>view and change properties for an object or collection of objects in a pane</strong>.</span></span></li>
<li><span data-ttu-id="84e30-128">Cuadro de diálogo Opciones: se usa para <strong>ver y cambiar las opciones de una aplicación</strong>.</span><span class="sxs-lookup"><span data-stu-id="84e30-128">Options dialog box: used to <strong>view and change options for an application</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

