---
description: Msimerg.exe es una utilidad de línea de comandos que usa MsiDatabaseMerge para combinar una base de datos de referencia en una base de datos base.
ms.assetid: db0c9ae5-a8e8-4eff-ae14-67dcce352483
title: Msimerg.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0555aa7bd762b92ed67d0bac1487159fadb73a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002773"
---
# <a name="msimergexe"></a><span data-ttu-id="dd469-103">Msimerg.exe</span><span class="sxs-lookup"><span data-stu-id="dd469-103">Msimerg.exe</span></span>

<span data-ttu-id="dd469-104">Msimerg.exe es una utilidad de línea de comandos que usa [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) para [combinar](merges-and-transforms.md) una base de datos de referencia en una base de datos base.</span><span class="sxs-lookup"><span data-stu-id="dd469-104">Msimerg.exe is a command line utility that uses [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to [merge](merges-and-transforms.md) a reference database into a base database.</span></span>

<span data-ttu-id="dd469-105">Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="dd469-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd469-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd469-106">Syntax</span></span>

<span data-ttu-id="dd469-107">**Msimerg** *{base Database} {base de datos de referencia}*</span><span class="sxs-lookup"><span data-stu-id="dd469-107">**Msimerg** *{base database}{reference database}*</span></span>

<span data-ttu-id="dd469-108">Si hay un conflicto de fusión mediante combinación entre las dos bases de datos, la información de conflictos se coloca en la \_ tabla MergeErrors.</span><span class="sxs-lookup"><span data-stu-id="dd469-108">If there is a merge conflict between the two databases, the conflict information is placed in the \_MergeErrors table.</span></span>

## <a name="command-line-options"></a><span data-ttu-id="dd469-109">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="dd469-109">Command Line Options</span></span>

<span data-ttu-id="dd469-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd469-110">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd469-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd469-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd469-112">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="dd469-112">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="dd469-113">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="dd469-113">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



