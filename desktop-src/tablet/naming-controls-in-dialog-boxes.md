---
description: Al usar cuadros de diálogo de Microsoft Windows, debe etiquetar todos los controles para facilitar la funcionalidad de voz. El siguiente cuadro de diálogo de ejecución muestra una etiqueta de control de texto estático para un cuadro de lista desplegable. El texto estático termina con un signo de dos puntos.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Asignar nombres a controles en cuadros de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104570697"
---
# <a name="naming-controls-in-dialog-boxes"></a><span data-ttu-id="453b6-105">Asignar nombres a controles en cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="453b6-105">Naming Controls in Dialog Boxes</span></span>

<span data-ttu-id="453b6-106">Al usar cuadros de diálogo de Microsoft Windows, debe etiquetar todos los controles para facilitar la funcionalidad de voz.</span><span class="sxs-lookup"><span data-stu-id="453b6-106">When using Microsoft Windows dialog boxes, you must label all controls to facilitate speech functionality.</span></span> <span data-ttu-id="453b6-107">El siguiente cuadro de diálogo de **ejecución** muestra una etiqueta de control de texto estático para un cuadro de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="453b6-107">The following **Run** dialog box shows a static text control label for a drop-down list box.</span></span> <span data-ttu-id="453b6-108">El texto estático termina con un signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="453b6-108">Static text ends with a colon.</span></span>

![captura de pantalla que muestra el cuadro de diálogo Ejecutar](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

<span data-ttu-id="453b6-110">Existen dos tipos de controles:</span><span class="sxs-lookup"><span data-stu-id="453b6-110">There are two types of controls:</span></span>

-   <span data-ttu-id="453b6-111">Controles que tienen sus títulos como propiedad de ese control, como botones de comando y casillas.</span><span class="sxs-lookup"><span data-stu-id="453b6-111">Controls that have their captions as a property of that control, such as command buttons and check boxes.</span></span> <span data-ttu-id="453b6-112">Las ayudas de accesibilidad no tienen ningún problema al identificar estos controles, siempre que el título esté definido correctamente.</span><span class="sxs-lookup"><span data-stu-id="453b6-112">Accessibility aids have no trouble identifying these controls as long as the caption is properly defined.</span></span>
-   <span data-ttu-id="453b6-113">Los controles que no tienen sus propios títulos, como controles de edición, cuadros de lista y vistas de lista, deben etiquetarse mediante controles de texto estático independientes.</span><span class="sxs-lookup"><span data-stu-id="453b6-113">Controls that do not have their own captions, such as edit controls, list boxes and list views, must be labeled by using separate static text controls.</span></span> <span data-ttu-id="453b6-114">Para obtener más información sobre los controles que no tienen sus propios títulos, vea [controles sin propiedades de título](controls-without-caption-properties.md).</span><span class="sxs-lookup"><span data-stu-id="453b6-114">For more information about controls that do not have their own captions, see [Controls Without Caption Properties](controls-without-caption-properties.md).</span></span>

<span data-ttu-id="453b6-115">Se pueden usar varias técnicas para solucionar situaciones en las que los controles no tienen sus propios títulos, pero solo se aplican a las ventanas que se muestran en el administrador de cuadros de diálogo estándar (SDM).</span><span class="sxs-lookup"><span data-stu-id="453b6-115">Several techniques can be used to overcome situations in which controls do not have their own captions, but they are only effective for windows that are displayed by the Standard Dialog Manager (SDM).</span></span> <span data-ttu-id="453b6-116">Todas las demás ventanas deben exponer los nombres y la relación entre los controles que admiten explícitamente Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="453b6-116">All other windows need to expose the names and relationship between controls by explicitly supporting Microsoft Active Accessibility.</span></span> <span data-ttu-id="453b6-117">Para obtener más información acerca de Active Accessibility, vea la sección de [accesibilidad](/windows/desktop/accessibility) de MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="453b6-117">For more information about Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section of the MSDN Library.</span></span>

 

 
