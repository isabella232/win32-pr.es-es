---
description: En este tema se describen las diferencias entre las versiones binarias de la biblioteca de Tablet PC.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: La versión de la biblioteca a la que se hace referencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696332"
---
# <a name="which-library-version-to-reference"></a><span data-ttu-id="e1416-103">La versión de la biblioteca a la que se hace referencia</span><span class="sxs-lookup"><span data-stu-id="e1416-103">Which Library Version to Reference</span></span>

<span data-ttu-id="e1416-104">En este tema se describen las diferencias entre las versiones binarias de la biblioteca de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e1416-104">This topic describes the differences between the Tablet PC library binary versions.</span></span>

## <a name="tablet-pc-library-versions"></a><span data-ttu-id="e1416-105">Versiones de la biblioteca de Tablet PC</span><span class="sxs-lookup"><span data-stu-id="e1416-105">Tablet PC Library Versions</span></span>

<span data-ttu-id="e1416-106">Los archivos binarios de la biblioteca de Tablet PC (Microsoft.Ink.dll) se han actualizado en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e1416-106">The Tablet PC library binaries (Microsoft.Ink.dll) have been updated in Windows Vista.</span></span> <span data-ttu-id="e1416-107">Estos archivos binarios se conocen como "versión 6,0" para incide con la versión de Windows en la que se publican.</span><span class="sxs-lookup"><span data-stu-id="e1416-107">Theses binaries are referred to as "version 6.0" to co-incide with the version of Windows in which they are being released.</span></span>

<span data-ttu-id="e1416-108">La versión más reciente de los binarios que son compatibles con Windows XP se conoce como "versión 1,7".</span><span class="sxs-lookup"><span data-stu-id="e1416-108">The most recent release of the binaries that are compatible with Windows XP is referred to as "version 1.7".</span></span>

<span data-ttu-id="e1416-109">El Windows SDK se puede instalar en las máquinas con vista y XP, y el Windows SDK incluye ambas versiones de Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="e1416-109">The Windows SDK can be installed on both Vista and XP machines, and the Windows SDK includes both versions of Microsoft.Ink.dll.</span></span>

<span data-ttu-id="e1416-110">Se instalan en:</span><span class="sxs-lookup"><span data-stu-id="e1416-110">These are installed in:</span></span>

1. <span data-ttu-id="e1416-111">% programfiles% \\ Reference assemblies \\ Microsoft \\ Tablet PC \\ v 1.7 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="e1416-111">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v1.7\\Microsoft.Ink.dll</span></span>

2. <span data-ttu-id="e1416-112">% programfiles% de \\ ensamblados de referencia \\ Microsoft \\ Tablet PC \\ v 6.0 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="e1416-112">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v6.0\\Microsoft.Ink.dll</span></span>

<span data-ttu-id="e1416-113">Los archivos binarios de la versión 6,0 solo son compatibles con Windows Vista y las aplicaciones escritas en ellos solo deben ejecutarse en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e1416-113">The version 6.0 binaries are only compatible with Windows Vista, and applications written against them should only ever be run on Windows Vista.</span></span>

<span data-ttu-id="e1416-114">Una aplicación escrita en los archivos binarios de la versión 1,7 debe ejecutarse sin modificaciones cuando se instala en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e1416-114">An application written against the version 1.7 binaries should run without modification when installed on Windows Vista.</span></span>

 

 



