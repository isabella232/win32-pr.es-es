---
description: En los sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas que se compilan para sistemas de 32 bits o de 64 bits.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Uso de acciones personalizadas de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002361"
---
# <a name="using-64-bit-custom-actions"></a><span data-ttu-id="e08c6-103">Uso de acciones personalizadas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="e08c6-103">Using 64-bit Custom Actions</span></span>

<span data-ttu-id="e08c6-104">En los sistemas operativos de 64 bits, Windows Installer puede llamar a acciones personalizadas que se compilan para sistemas de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e08c6-104">On 64-bit operating systems, Windows Installer can call custom actions that are compiled for 32-bit or 64-bit systems.</span></span> <span data-ttu-id="e08c6-105">Una acción personalizada de 64 bits basada en [scripts](scripts.md) debe marcarse explícitamente como una acción personalizada de 64 bits agregando el bit **msidbCustomActionType64BitScript** al tipo numérico de la acción personalizada en la columna tipo de la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="e08c6-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom action numeric type in the Type column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="e08c6-106">Las acciones personalizadas basadas en [archivos ejecutables](executable-files.md) o [bibliotecas de vínculos dinámicos](dynamic-link-libraries.md) que se cumplen para los sistemas operativos de 64 bits no requieren que se incluya este bit adicional en la columna tipo de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="e08c6-106">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that are complied for 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction Table.</span></span>

<span data-ttu-id="e08c6-107">Para obtener más información, consulte [acciones personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="e08c6-107">For more information, see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

 

 



