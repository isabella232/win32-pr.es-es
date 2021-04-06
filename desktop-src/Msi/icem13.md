---
description: ICEM13 comprueba que el módulo de combinación no contiene ensamblados de configuración y directivas de edición.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909022"
---
# <a name="icem13"></a><span data-ttu-id="4481e-103">ICEM13</span><span class="sxs-lookup"><span data-stu-id="4481e-103">ICEM13</span></span>

<span data-ttu-id="4481e-104">ICEM13 comprueba que el módulo de combinación no contiene ensamblados de configuración y directivas de edición.</span><span class="sxs-lookup"><span data-stu-id="4481e-104">ICEM13 verifies that the merge module does not contain publisher policy and configuration assemblies.</span></span> <span data-ttu-id="4481e-105">La Directiva del publicador y los ensamblados de configuración no deben incluirse en los módulos de combinación destinados a la redistribución, ya que esto puede afectar a otras aplicaciones en el equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="4481e-105">Publisher policy and configuration assemblies should not be included in merge modules intended for redistribution because this can affect other applications on a user's computer.</span></span>

<span data-ttu-id="4481e-106">Este ICEM está disponible en el archivo Mergemod. Cub proporcionado en el SDK de Windows Installer 2,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4481e-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="4481e-107">Para obtener más información, consulte [componentes de Windows SDK para desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="4481e-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="4481e-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="4481e-108">Result</span></span>

<span data-ttu-id="4481e-109">ICEM13 envía un mensaje de ADVERTENCIA Si encuentra un componente especificado en el campo componente de la [tabla MsiAssembly](msiassembly-table.md) del módulo de combinación, que es una directiva de edición o un ensamblado de configuración.</span><span class="sxs-lookup"><span data-stu-id="4481e-109">ICEM13 posts a warning message if it finds a component specified in the Component field of the merge module's [MsiAssembly Table](msiassembly-table.md) that is a publisher policy or configuration assembly.</span></span>

## <a name="example"></a><span data-ttu-id="4481e-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4481e-110">Example</span></span>

<span data-ttu-id="4481e-111">ICEM13 envía el siguiente mensaje de ADVERTENCIA Si encuentra una fila en la [tabla MsiAssembly](msiassembly-table.md) con un componente ' \[ 1 \] ' especificado en el campo componente que es una directiva de edición o un ensamblado de configuración que se ha incluido en el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="4481e-111">ICEM13 posts the following warning message if it finds a row in the [MsiAssembly Table](msiassembly-table.md) with a component '\[1\]' specified in the Component field that is a publisher policy or configuration assembly that has been included in the merge module.</span></span>

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

<span data-ttu-id="4481e-112">Es posible instalar la Directiva del publicador y los ensamblados de configuración mediante el Windows Installer, no se recomienda que estos ensamblados se redistribuyan en módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="4481e-112">It is possible to install publisher policy and configuration assemblies using the Windows Installer, it is not recommended that these assemblies be redistributed in merge modules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4481e-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4481e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4481e-114">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="4481e-114">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



