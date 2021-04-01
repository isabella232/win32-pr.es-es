---
description: Un paquete de 64 bits se compone parcial o totalmente de componentes de Windows Installer de 64 bits.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: Paquetes de Windows Installer de bits de 64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909158"
---
# <a name="64-bit-windows-installer-packages"></a><span data-ttu-id="c3a34-103">Paquetes de Windows Installer de bits de 64</span><span class="sxs-lookup"><span data-stu-id="c3a34-103">64-bit Windows Installer Packages</span></span>

<span data-ttu-id="c3a34-104">Un paquete de 64 bits se compone parcial o totalmente de componentes de [Windows Installer](windows-installer-components.md) de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c3a34-104">A 64-bit package consists partially or entirely of 64-bit [Windows Installer](windows-installer-components.md) components.</span></span> <span data-ttu-id="c3a34-105">En la lista siguiente se identifican los requisitos para cada paquete de Windows Installer de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="c3a34-105">The following list identifies the requirements for every 64-bit Windows Installer package:</span></span>

-   <span data-ttu-id="c3a34-106">El valor "Intel64" debe especificarse en el campo Platform de la propiedad de Resumen de la [**plantilla**](template-summary.md) si y solo si el paquete se ejecuta en un procesador Intel64 (Itanium).</span><span class="sxs-lookup"><span data-stu-id="c3a34-106">The value "Intel64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Intel64 (Itanium) processor.</span></span>
-   <span data-ttu-id="c3a34-107">El valor "x64" se debe escribir en el campo plataforma de la propiedad de Resumen de la [**plantilla**](template-summary.md) si y solo si el paquete se ejecuta en un procesador x64.</span><span class="sxs-lookup"><span data-stu-id="c3a34-107">The value "x64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an x64 processor.</span></span>
-   <span data-ttu-id="c3a34-108">El valor "Arm64" debe especificarse en el campo Platform de la propiedad de Resumen de la [**plantilla**](template-summary.md) si y solo si el paquete se ejecuta en un procesador Arm64.</span><span class="sxs-lookup"><span data-stu-id="c3a34-108">The value "Arm64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Arm64 processor.</span></span>
-   <span data-ttu-id="c3a34-109">La propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) se debe establecer en el entero 200 o superior, porque Windows Installer 2,0 es la versión mínima que es capaz de instalar componentes de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c3a34-109">The [**Page Count Summary**](page-count-summary.md) property must be set to the integer 200 or greater, because Windows Installer 2.0 is the minimum version that is capable of installing 64-bit components.</span></span> <span data-ttu-id="c3a34-110">Los paquetes de la plataforma Arm64 requieren un valor de 500 o superior.</span><span class="sxs-lookup"><span data-stu-id="c3a34-110">Packages for the Arm64 platform require a value of 500 or greater.</span></span>
-   <span data-ttu-id="c3a34-111">Cada componente de Windows Installer de 64 bits del paquete debe incluir el bit **msidbComponentAttributes64bit** en la columna Attributes de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3a34-111">Each 64-bit Windows Installer component in the package must include the **msidbComponentAttributes64bit** bit in the Attributes column of the [Component Table](component-table.md).</span></span>

<span data-ttu-id="c3a34-112">Para obtener más información, consulte [Windows Installer en sistemas operativos de 64](windows-installer-on-64-bit-operating-systems.md) bits y [paquetes de Windows Installer de 32 bits](32-bit-windows-installer-packages.md).</span><span class="sxs-lookup"><span data-stu-id="c3a34-112">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md) and [32-bit Windows Installer Packages](32-bit-windows-installer-packages.md).</span></span>

 

 



