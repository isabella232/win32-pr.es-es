---
title: Generar un cuadro de diálogo para seleccionar un formato para guardar
description: Generar un cuadro de diálogo para seleccionar un formato para guardar
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- Administrador de compresión de audio (ACM), generar cuadros de diálogo
- ACM (Administrador de compresión de audio), generar cuadros de diálogo
- Ejemplos de ACM, generar cuadros de diálogo
- generar cuadros de diálogo
- acmFormatChoose función)
- Administrador de compresión de audio (ACM), seleccionar formato para guardar
- ACM (Administrador de compresión de audio), seleccionar formato para guardar
- Ejemplos de ACM, seleccionar formato para guardar
- Seleccionar formato para guardar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55df4cd89a04bf1d3dd34512c4014928b6d5d4fb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/27/2020
ms.locfileid: "104420381"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a><span data-ttu-id="466e4-112">Generar un cuadro de diálogo para seleccionar un formato para guardar</span><span class="sxs-lookup"><span data-stu-id="466e4-112">Producing a Dialog Box for Selecting a Format for Saving</span></span>

<span data-ttu-id="466e4-113">Es posible que desee que una aplicación guarde los datos de audio de forma de onda existentes en otro formato.</span><span class="sxs-lookup"><span data-stu-id="466e4-113">You might want an application to save existing waveform-audio data in another format.</span></span> <span data-ttu-id="466e4-114">Por ejemplo, un editor de audio de forma de onda podría guardar un archivo de audio de forma de onda como archivo comprimido.</span><span class="sxs-lookup"><span data-stu-id="466e4-114">For example, a waveform-audio editor could save a waveform-audio file as a compressed file.</span></span> <span data-ttu-id="466e4-115">Para mostrar solo los formatos de destino sugeridos para un formato de origen especificado en el cuadro de diálogo creado por la función [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , especifique el formato de origen en el miembro **pwfxEnum** y el \_ marcador ACM FORMATENUMF \_ sugerir en el miembro **fdwEnum** de la estructura [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="466e4-115">To list only the suggested destination formats for a specified source format in the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specify the source format in the **pwfxEnum** member and the ACM\_FORMATENUMF\_SUGGEST flag in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

<span data-ttu-id="466e4-116">Del mismo modo, para obtener una lista de formatos de destino válidos para un formato especificado, use la \_ marca de conversión ACM FORMATENUMF \_ en lugar de la \_ marca de sugerencia FORMATENUMF de ACM \_ .</span><span class="sxs-lookup"><span data-stu-id="466e4-116">Similarly, to list valid destination formats for a specified format, use the ACM\_FORMATENUMF\_CONVERT flag instead of the ACM\_FORMATENUMF\_SUGGEST flag.</span></span>

 

 




