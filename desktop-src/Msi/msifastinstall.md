---
description: La propiedad MSIFASTINSTALL se puede usar para reducir el tiempo necesario para instalar un paquete de Windows Installer grande.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Propiedad MSIFASTINSTALL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653707"
---
# <a name="msifastinstall-property"></a><span data-ttu-id="54501-103">Propiedad MSIFASTINSTALL</span><span class="sxs-lookup"><span data-stu-id="54501-103">MSIFASTINSTALL property</span></span>

<span data-ttu-id="54501-104">La propiedad **MSIFASTINSTALL** se puede usar para reducir el tiempo necesario para instalar un paquete de Windows Installer grande.</span><span class="sxs-lookup"><span data-stu-id="54501-104">The **MSIFASTINSTALL** property can be used to reduce the time required to install a large Windows Installer package.</span></span> <span data-ttu-id="54501-105">La propiedad se puede establecer en la línea de comandos o en la tabla de [propiedades](property-table.md) para configurar las operaciones que el usuario o desarrollador determina que no son esenciales para la instalación.</span><span class="sxs-lookup"><span data-stu-id="54501-105">The property can be set on the command line or in the [Property](property-table.md) table to configure operations that the user or developer determines are non-essential for the installation.</span></span>

<span data-ttu-id="54501-106">El valor de la propiedad **MSIFASTINSTALL** puede ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="54501-106">The value of the **MSIFASTINSTALL** property can be a combination of the following values.</span></span>



| <span data-ttu-id="54501-107">Value</span><span class="sxs-lookup"><span data-stu-id="54501-107">Value</span></span> | <span data-ttu-id="54501-108">Significado</span><span class="sxs-lookup"><span data-stu-id="54501-108">Meaning</span></span>                                                                      |
|-------|------------------------------------------------------------------------------|
| <span data-ttu-id="54501-109">0</span><span class="sxs-lookup"><span data-stu-id="54501-109">0</span></span>     | <span data-ttu-id="54501-110">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="54501-110">Default value</span></span>                                                                |
| <span data-ttu-id="54501-111">1</span><span class="sxs-lookup"><span data-stu-id="54501-111">1</span></span>     | <span data-ttu-id="54501-112">No se ha guardado ningún punto de restauración del sistema para esta instalación.</span><span class="sxs-lookup"><span data-stu-id="54501-112">No system restore point is saved for this installation.</span></span>                      |
| <span data-ttu-id="54501-113">2</span><span class="sxs-lookup"><span data-stu-id="54501-113">2</span></span>     | <span data-ttu-id="54501-114">Realizar solo los [costos de archivos](file-costing.md) y omitir la comprobación de otros costos.</span><span class="sxs-lookup"><span data-stu-id="54501-114">Perform only [File Costing](file-costing.md) and skip checking other costs.</span></span> |
| <span data-ttu-id="54501-115">4</span><span class="sxs-lookup"><span data-stu-id="54501-115">4</span></span>     | <span data-ttu-id="54501-116">Reducir la frecuencia de los mensajes de progreso.</span><span class="sxs-lookup"><span data-stu-id="54501-116">Reduce the frequency of progress messages.</span></span>                                   |



 

<span data-ttu-id="54501-117">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="54501-117">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="54501-118">Esta propiedad está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="54501-118">This property is available beginning with Windows Installer 5.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="54501-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54501-119">Requirements</span></span>



| <span data-ttu-id="54501-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="54501-120">Requirement</span></span> | <span data-ttu-id="54501-121">Value</span><span class="sxs-lookup"><span data-stu-id="54501-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54501-122">Versión</span><span class="sxs-lookup"><span data-stu-id="54501-122">Version</span></span><br/> | <span data-ttu-id="54501-123">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="54501-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="54501-124">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="54501-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



 

 




