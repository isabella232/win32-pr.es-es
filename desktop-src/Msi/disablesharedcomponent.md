---
description: Si esta Directiva del sistema por equipo está establecida en 1, ningún paquete del sistema obtiene la funcionalidad del componente compartido habilitada por el atributo msidbComponentAttributesShared en la tabla de componentes.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542742"
---
# <a name="disablesharedcomponent"></a><span data-ttu-id="3db82-103">DisableSharedComponent</span><span class="sxs-lookup"><span data-stu-id="3db82-103">DisableSharedComponent</span></span>

<span data-ttu-id="3db82-104">Si esta [Directiva del sistema](system-policy.md) por equipo está establecida en 1, ningún paquete del sistema obtiene la funcionalidad del componente compartido habilitada por el atributo **msidbComponentAttributesShared** en la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="3db82-104">If this per-machine [system policy](system-policy.md) is set to 1, no package on the system gets the shared component functionality enabled by the **msidbComponentAttributesShared** attribute in the [Component table](component-table.md).</span></span> <span data-ttu-id="3db82-105">El valor predeterminado es 0, que habilita la funcionalidad de componentes compartidos para los componentes marcados con **msidbComponentAttributesShared** en todos los paquetes.</span><span class="sxs-lookup"><span data-stu-id="3db82-105">The default value is 0, which enables the shared component functionality for components marked with **msidbComponentAttributesShared** in all packages.</span></span>

<span data-ttu-id="3db82-106">**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="3db82-106">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="3db82-107">Esta función está disponible a partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="3db82-107">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="3db82-108">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="3db82-108">Registry Key</span></span>

<span data-ttu-id="3db82-109">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="3db82-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="3db82-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3db82-110">Data Type</span></span>

<span data-ttu-id="3db82-111">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="3db82-111">**REG\_DWORD**</span></span>

 

 



