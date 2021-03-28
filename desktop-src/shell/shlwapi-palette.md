---
description: En esta sección se describen las funciones de control de la paleta de colores de Shell de Windows. Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.
title: Funciones de control de la paleta de colores de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 93848cb3-60c6-4b2f-82d9-abfee97e372a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba92dcf280b8d54b8778e276bb603d888f5991c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277222"
---
# <a name="shell-color-palette-handling-functions"></a><span data-ttu-id="d7211-104">Funciones de control de la paleta de colores de Shell</span><span class="sxs-lookup"><span data-stu-id="d7211-104">Shell Color Palette Handling Functions</span></span>

<span data-ttu-id="d7211-105">En esta sección se describen las funciones de control de la paleta de colores de Shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="d7211-105">This section describes the Windows Shell color palette handling functions.</span></span> <span data-ttu-id="d7211-106">Los elementos de programación que se explican en esta documentación se exportan mediante Shlwapi.dll y se definen en shlwapi. h y shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="d7211-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d7211-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d7211-107">In this section</span></span>



| <span data-ttu-id="d7211-108">Tema</span><span class="sxs-lookup"><span data-stu-id="d7211-108">Topic</span></span>                                                           | <span data-ttu-id="d7211-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7211-109">Description</span></span>                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7211-110">**ColorAdjustLuma**</span><span class="sxs-lookup"><span data-stu-id="d7211-110">**ColorAdjustLuma**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-coloradjustluma)<br/>           | <span data-ttu-id="d7211-111">Cambia la luminancia de un valor RGB.</span><span class="sxs-lookup"><span data-stu-id="d7211-111">Changes the luminance of a RGB value.</span></span> <span data-ttu-id="d7211-112">El matiz y la saturación no se ven afectados.</span><span class="sxs-lookup"><span data-stu-id="d7211-112">Hue and saturation are not affected.</span></span><br/> |
| [<span data-ttu-id="d7211-113">**ColorHLSToRGB**</span><span class="sxs-lookup"><span data-stu-id="d7211-113">**ColorHLSToRGB**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorhlstorgb)<br/>               | <span data-ttu-id="d7211-114">Convierte los colores de Hue-luminancia-saturación (HLS) al formato RGB.</span><span class="sxs-lookup"><span data-stu-id="d7211-114">Converts colors from hue-luminance-saturation (HLS) to RGB format.</span></span><br/>         |
| [<span data-ttu-id="d7211-115">**ColorRGBToHLS**</span><span class="sxs-lookup"><span data-stu-id="d7211-115">**ColorRGBToHLS**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorrgbtohls)<br/>               | <span data-ttu-id="d7211-116">Convierte los colores del formato RGB a Hue-luminancia-saturación (HLS).</span><span class="sxs-lookup"><span data-stu-id="d7211-116">Converts colors from RGB to hue-luminance-saturation (HLS) format.</span></span><br/>         |
| [<span data-ttu-id="d7211-117">**SHCreateShellPalette**</span><span class="sxs-lookup"><span data-stu-id="d7211-117">**SHCreateShellPalette**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreateshellpalette)<br/> | <span data-ttu-id="d7211-118">Crea una paleta de semitonos para el contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d7211-118">Creates a halftone palette for the specified device context.</span></span><br/>               |



 

 

 




