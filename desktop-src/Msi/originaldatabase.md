---
description: El Windows Installer establece la propiedad OriginalDatabase en la ruta de acceso de la base de datos de instalación que se usa para iniciar la instalación.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Propiedad OriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679525"
---
# <a name="originaldatabase-property"></a><span data-ttu-id="0c85b-103">Propiedad OriginalDatabase</span><span class="sxs-lookup"><span data-stu-id="0c85b-103">OriginalDatabase property</span></span>

<span data-ttu-id="0c85b-104">El Windows Installer establece la propiedad **OriginalDatabase** en la ruta de acceso de la base de datos de instalación que se usa para iniciar la instalación.</span><span class="sxs-lookup"><span data-stu-id="0c85b-104">The Windows Installer sets the **OriginalDatabase** property to the path of the installation database used to launch the installation.</span></span> <span data-ttu-id="0c85b-105">Si la instalación se inicia desde una línea de comandos, el valor depende de si la opción de paquete para volver a almacenar en caché (la marca-v) está presente en la propiedad [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="0c85b-105">If the installation is launched from a command line, the value depends on whether the recache package option (the -v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>



| <span data-ttu-id="0c85b-106">Método de instalación</span><span class="sxs-lookup"><span data-stu-id="0c85b-106">Installation Method</span></span>                                                                                                                                                                                  | <span data-ttu-id="0c85b-107">Valor OriginalDatabase</span><span class="sxs-lookup"><span data-stu-id="0c85b-107">OriginalDatabase Value</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="0c85b-108">Cualquier instalación iniciada mediante la invocación de la ruta de acceso del paquete de instalación (archivo. msi).</span><span class="sxs-lookup"><span data-stu-id="0c85b-108">Any installation launched by invoking the path of the installation package (.msi file).</span></span>                                                                                                              | <span data-ttu-id="0c85b-109">Ruta de acceso al paquete de instalación (archivo. msi).</span><span class="sxs-lookup"><span data-stu-id="0c85b-109">Path to the installation package (.msi file).</span></span> |
| <span data-ttu-id="0c85b-110">Instalación iniciada desde una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0c85b-110">Installation launched from a command line.</span></span> <span data-ttu-id="0c85b-111">La instalación no se inicia desde una ruta de acceso del paquete.</span><span class="sxs-lookup"><span data-stu-id="0c85b-111">The installation is not launched from a package path.</span></span> <span data-ttu-id="0c85b-112">La opción recache (-v flag) está presente en la propiedad [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="0c85b-112">The recache option (-v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>     | <span data-ttu-id="0c85b-113">Ruta de acceso a la base de datos en el origen.</span><span class="sxs-lookup"><span data-stu-id="0c85b-113">Path to the database on the source.</span></span>           |
| <span data-ttu-id="0c85b-114">Instalación iniciada desde una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0c85b-114">Installation launched from a command line.</span></span> <span data-ttu-id="0c85b-115">La instalación no se inicia desde una ruta de acceso del paquete.</span><span class="sxs-lookup"><span data-stu-id="0c85b-115">The installation is not launched from a package path.</span></span> <span data-ttu-id="0c85b-116">La opción recache (-v flag) no está presente en la propiedad [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="0c85b-116">The recache option (-v flag) is not present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> | <span data-ttu-id="0c85b-117">Ruta de acceso a la base de datos almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="0c85b-117">Path to the cached database.</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="0c85b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c85b-118">Remarks</span></span>

<span data-ttu-id="0c85b-119">Durante una instalación por primera vez, una acción personalizada se secuencia antes de la [acción ResolveSource](resolvesource-action.md) puede usar la propiedad **OriginalDatabase** para determinar la ubicación del origen de instalación.</span><span class="sxs-lookup"><span data-stu-id="0c85b-119">During a first time installation, a custom action sequenced before the [ResolveSource action](resolvesource-action.md) can use the **OriginalDatabase** property to determine the location of the installation source.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c85b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c85b-120">Requirements</span></span>



| <span data-ttu-id="0c85b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c85b-121">Requirement</span></span> | <span data-ttu-id="0c85b-122">Value</span><span class="sxs-lookup"><span data-stu-id="0c85b-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c85b-123">Versión</span><span class="sxs-lookup"><span data-stu-id="0c85b-123">Version</span></span><br/> | <span data-ttu-id="0c85b-124">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c85b-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0c85b-125">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0c85b-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0c85b-126">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0c85b-126">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0c85b-127">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0c85b-127">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c85b-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0c85b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c85b-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c85b-129">Properties</span></span>](properties.md)
</dt> </dl>

 

 




