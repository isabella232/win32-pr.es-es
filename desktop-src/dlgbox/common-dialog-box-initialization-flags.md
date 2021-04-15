---
title: Marcas de inicialización comunes de cuadros de diálogo
description: Las marcas se usan para modificar el comportamiento y la apariencia de un cuadro de diálogo común.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Biblioteca de cuadros de diálogo comunes, inicializar
- cuadros de diálogo comunes, inicializar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/19/2020
ms.locfileid: "104488621"
---
# <a name="common-dialog-box-initialization-flags"></a><span data-ttu-id="0f4f9-105">Marcas de inicialización comunes de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="0f4f9-105">Common Dialog Box Initialization Flags</span></span>

<span data-ttu-id="0f4f9-106">Las marcas se usan para modificar el comportamiento y la apariencia de un cuadro de diálogo común.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-106">Flags are used to modify the behavior and appearance of a common dialog box.</span></span> <span data-ttu-id="0f4f9-107">Las marcas de inicialización son los valores que se establecen en el miembro **Flags** de la estructura que se usa para crear el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-107">Initialization flags are the values that you set in the **Flags** member of the structure that is used to create the dialog box.</span></span> <span data-ttu-id="0f4f9-108">Las marcas se usan para especificar qué controles de un cuadro de diálogo reciben valores iniciales, para deshabilitar los controles seleccionados y para modificar el intervalo de valores que el usuario puede establecer con los controles.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-108">You use the flags to specify which controls in a dialog box receive initial values, to disable selected controls, and to modify the range of values that the user can set with the controls.</span></span> <span data-ttu-id="0f4f9-109">También puede usar las marcas para habilitar procedimientos de enlace y plantillas personalizadas para los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-109">You also use the flags to enable hook procedures and custom templates for the dialog boxes.</span></span>

<span data-ttu-id="0f4f9-110">Por ejemplo, puede establecer el valor de los **\_ efectos de CF** en el miembro **Flags** de la estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para dirigir el cuadro de diálogo **fuente** para mostrar los controles de efectos.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-110">For example, you can set the **CF\_EFFECTS** value in the **Flags** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to direct the **Font** dialog box to display the effects controls.</span></span> <span data-ttu-id="0f4f9-111">Estos controles permiten al usuario elegir un color de fuente, así como efectos de tachado y subrayado.</span><span class="sxs-lookup"><span data-stu-id="0f4f9-111">These controls let the user choose a font color as well as strikethrough and underline effects.</span></span>

<span data-ttu-id="0f4f9-112">Los valores de la marca de inicialización son únicos para cada cuadro de diálogo común y se describen en detalle mediante los miembros de **marcas** de las siguientes estructuras que se corresponden con ellos:</span><span class="sxs-lookup"><span data-stu-id="0f4f9-112">The initialization flag values are unique to each common dialog box and are described in detail by the **Flags** members of the following structures that correspond to them:</span></span>

-   [<span data-ttu-id="0f4f9-113">**LAS CHOOSECOLOR.**</span><span class="sxs-lookup"><span data-stu-id="0f4f9-113">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [<span data-ttu-id="0f4f9-114">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="0f4f9-114">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="0f4f9-115">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="0f4f9-115">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [<span data-ttu-id="0f4f9-116">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="0f4f9-116">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [<span data-ttu-id="0f4f9-117">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="0f4f9-117">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [<span data-ttu-id="0f4f9-118">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="0f4f9-118">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [<span data-ttu-id="0f4f9-119">**PRINTDLGEX**</span><span class="sxs-lookup"><span data-stu-id="0f4f9-119">**PRINTDLGEX**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




