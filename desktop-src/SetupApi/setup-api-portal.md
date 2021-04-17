---
description: Instala controladores de dispositivos desde programas con un script de configuración y archivos INF. Escribir un programa de instalación para la configuración del dispositivo y la instalación del controlador. Esta API ya no se recomienda para la instalación de aplicaciones de software.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: API de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667604"
---
# <a name="setup-api"></a><span data-ttu-id="bd603-105">API de configuración</span><span class="sxs-lookup"><span data-stu-id="bd603-105">Setup API</span></span>

## <a name="purpose"></a><span data-ttu-id="bd603-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="bd603-106">Purpose</span></span>

<span data-ttu-id="bd603-107">La API de instalación proporciona un conjunto de funciones que una aplicación de instalación llama para realizar operaciones de instalación.</span><span class="sxs-lookup"><span data-stu-id="bd603-107">The Setup API provides a set of functions that a setup application calls to perform installation operations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="bd603-108">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="bd603-108">Where applicable</span></span>

<span data-ttu-id="bd603-109">Estas funciones de configuración están disponibles para desarrollar una aplicación de instalación.</span><span class="sxs-lookup"><span data-stu-id="bd603-109">These setup functions are available to develop a setup application.</span></span> <span data-ttu-id="bd603-110">La API de instalación ya no debe usarse para instalar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bd603-110">Setup API should no longer be used for installing applications.</span></span> <span data-ttu-id="bd603-111">En su lugar, use el [Windows Installer](/windows/desktop/Msi/windows-installer-portal)para desarrollar instaladores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bd603-111">Instead, use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal)for developing application installers.</span></span> <span data-ttu-id="bd603-112">La API de instalación continúa utilizándose para instalar controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bd603-112">Setup API continues to be used for installing device drivers.</span></span>

<span data-ttu-id="bd603-113">La API de instalación está pensada para el desarrollo de aplicaciones de estilo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="bd603-113">The Setup API is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bd603-114">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="bd603-114">Developer audience</span></span>

<span data-ttu-id="bd603-115">Un desarrollador puede usar la API de instalación si su aplicación de instalación requiere la siguiente funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="bd603-115">A developer can use the Setup API if their setup application requires the following functionality:</span></span>

-   <span data-ttu-id="bd603-116">Puesta en cola de archivos.</span><span class="sxs-lookup"><span data-stu-id="bd603-116">Queuing of files.</span></span>
-   <span data-ttu-id="bd603-117">Instalación de archivos.</span><span class="sxs-lookup"><span data-stu-id="bd603-117">Installation of files.</span></span>
-   <span data-ttu-id="bd603-118">Control de los errores de instalación y solicitud de medios.</span><span class="sxs-lookup"><span data-stu-id="bd603-118">Handling of installation errors and prompting for media.</span></span>
-   <span data-ttu-id="bd603-119">Actualizando entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="bd603-119">Updating registry entries.</span></span>
-   <span data-ttu-id="bd603-120">Registro de archivos a medida que se instalan.</span><span class="sxs-lookup"><span data-stu-id="bd603-120">Logging of files as they are installed.</span></span>
-   <span data-ttu-id="bd603-121">Almacenamiento de las rutas de acceso de origen usadas más recientemente.</span><span class="sxs-lookup"><span data-stu-id="bd603-121">Storage of the most recently used source paths.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bd603-122">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="bd603-122">Run-time requirements</span></span>

<span data-ttu-id="bd603-123">Para obtener información acerca de los sistemas operativos necesarios para usar una función determinada, consulte la sección de requisitos de la documentación de la función.</span><span class="sxs-lookup"><span data-stu-id="bd603-123">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bd603-124">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bd603-124">In this section</span></span>



| <span data-ttu-id="bd603-125">Tema</span><span class="sxs-lookup"><span data-stu-id="bd603-125">Topic</span></span>                                 | <span data-ttu-id="bd603-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd603-126">Description</span></span>                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd603-127">Información general</span><span class="sxs-lookup"><span data-stu-id="bd603-127">Overview</span></span>](overview.md)<br/>   | <span data-ttu-id="bd603-128">Información general sobre la API de instalación.</span><span class="sxs-lookup"><span data-stu-id="bd603-128">General information about Setup API.</span></span><br/>                                             |
| [<span data-ttu-id="bd603-129">Referencia</span><span class="sxs-lookup"><span data-stu-id="bd603-129">Reference</span></span>](reference.md)<br/> | <span data-ttu-id="bd603-130">Documentación de los tipos de datos, las estructuras, las funciones y las notificaciones de la API de instalación.</span><span class="sxs-lookup"><span data-stu-id="bd603-130">Documentation of Setup API data types, structures, functions, and notifications.</span></span><br/> |



 

 

