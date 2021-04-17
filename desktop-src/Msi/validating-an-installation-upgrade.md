---
description: Siempre que realice cambios en el paquete, los autores de paquetes de actualización siempre deben ejecutar la validación en sus paquetes antes de intentar instalar el paquete por primera vez y volver a ejecutar la validación.
ms.assetid: c578c020-18be-47ea-8f59-c1bbd45f1260
title: Validar una actualización de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cab7f45d3d5c19a71dac8c7a2d0150409b3a45f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678587"
---
# <a name="validating-an-installation-upgrade"></a><span data-ttu-id="d38c2-103">Validar una actualización de instalación</span><span class="sxs-lookup"><span data-stu-id="d38c2-103">Validating an Installation Upgrade</span></span>

<span data-ttu-id="d38c2-104">Siempre que realice cambios en el paquete, los autores de paquetes de actualización siempre deben ejecutar la validación en sus paquetes antes de intentar instalar el paquete por primera vez y volver a ejecutar la validación.</span><span class="sxs-lookup"><span data-stu-id="d38c2-104">Whenever making any changes to the package, authors of upgrade packages should always run validation on their packages before attempting to install the package for the first time and rerun validation.</span></span> <span data-ttu-id="d38c2-105">Ejecutar la validación en un paquete de actualización de la misma manera que para un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="d38c2-105">Run validation on an upgrade package in the same way as for an installation package.</span></span> <span data-ttu-id="d38c2-106">Para obtener más información, consulte [validar una base de datos de instalación](validating-an-installation-database.md).</span><span class="sxs-lookup"><span data-stu-id="d38c2-106">For details, see [Validating an Installation Database](validating-an-installation-database.md).</span></span>

<span data-ttu-id="d38c2-107">Esto completa el paquete de actualización de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d38c2-107">This completes the sample upgrade package.</span></span> <span data-ttu-id="d38c2-108">Para instalar la primera instalación de la actualización MNP2000.msi y, a continuación, instale MNP2001.msi.</span><span class="sxs-lookup"><span data-stu-id="d38c2-108">To install the upgrade first install MNP2000.msi and then install MNP2001.msi.</span></span> <span data-ttu-id="d38c2-109">Al desinstalar MNP2001, los productos originales y de actualización se quitan del equipo.</span><span class="sxs-lookup"><span data-stu-id="d38c2-109">When you uninstall MNP2001 both the original and upgrade products are removed from your computer.</span></span>

## <a name="next-example"></a><span data-ttu-id="d38c2-110">Ejemplo siguiente</span><span class="sxs-lookup"><span data-stu-id="d38c2-110">Next example</span></span>

[<span data-ttu-id="d38c2-111">Ejemplo de transformación de personalización</span><span class="sxs-lookup"><span data-stu-id="d38c2-111">A Customization Transform Example</span></span>](a-customization-transform-example.md)

 

 



