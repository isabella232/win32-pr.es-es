---
description: En los sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas compiladas para sistemas de 32 bits o de 64 bits.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: Acciones personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813371"
---
# <a name="64-bit-custom-actions"></a><span data-ttu-id="cc557-103">Acciones personalizadas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="cc557-103">64-Bit Custom Actions</span></span>

<span data-ttu-id="cc557-104">En los sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas compiladas para sistemas de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cc557-104">On 64-bit operating systems, Windows Installer may call custom actions that have been compiled for 32-bit or 64-bit systems.</span></span>

<span data-ttu-id="cc557-105">Una acción personalizada de 64 bits basada en [scripts](scripts.md) debe marcarse explícitamente como una acción personalizada de 64 bits agregando el bit **msidbCustomActionType64BitScript** al tipo numérico Actions personalizado en la columna Type de la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="cc557-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction table](customaction-table.md).</span></span>



| <span data-ttu-id="cc557-106">Constante</span><span class="sxs-lookup"><span data-stu-id="cc557-106">Constant</span></span>                             | <span data-ttu-id="cc557-107">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="cc557-107">Hexadecimal</span></span> | <span data-ttu-id="cc557-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="cc557-108">Decimal</span></span> | <span data-ttu-id="cc557-109">Significado</span><span class="sxs-lookup"><span data-stu-id="cc557-109">Meaning</span></span>                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| <span data-ttu-id="cc557-110">**msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="cc557-110">**msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="cc557-111">0x0001000</span><span class="sxs-lookup"><span data-stu-id="cc557-111">0x0001000</span></span>   | <span data-ttu-id="cc557-112">4096</span><span class="sxs-lookup"><span data-stu-id="cc557-112">4096</span></span>    | <span data-ttu-id="cc557-113">Se trata de una acción personalizada de 64 bits escrita en [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="cc557-113">This is a 64-bit custom action written in [Scripts](scripts.md).</span></span> |



 

<span data-ttu-id="cc557-114">Las acciones personalizadas basadas en [archivos ejecutables](executable-files.md) o [bibliotecas de vínculos dinámicos](dynamic-link-libraries.md) que se han cumplido para los sistemas operativos de 64 bits no requieren incluir este bit adicional en la columna de tipo de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="cc557-114">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that have been complied for a 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction table.</span></span>

 

 



