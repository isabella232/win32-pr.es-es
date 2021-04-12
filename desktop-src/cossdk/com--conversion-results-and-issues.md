---
description: Tanto si decide convertir los paquetes MTS en aplicaciones COM+ manualmente como si desea que el proceso de instalación de Microsoft Windows lo haga automáticamente, debe tener en cuenta los resultados de la conversión, así como de los problemas.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Resultados y problemas de la conversión de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423503"
---
# <a name="com-conversion-results-and-issues"></a><span data-ttu-id="03680-103">Resultados y problemas de la conversión de COM+</span><span class="sxs-lookup"><span data-stu-id="03680-103">COM+ Conversion Results and Issues</span></span>

<span data-ttu-id="03680-104">Tanto si decide convertir los paquetes MTS en aplicaciones COM+ manualmente como si desea que el proceso de instalación de Microsoft Windows lo haga automáticamente, debe tener en cuenta los resultados de la conversión, así como de los problemas.</span><span class="sxs-lookup"><span data-stu-id="03680-104">Whether you choose to convert your MTS packages to COM+ applications manually or let the Microsoft Windows setup process do it for you automatically, you should be aware of the results of conversion as well as the issues.</span></span>

## <a name="what-is-converted"></a><span data-ttu-id="03680-105">Lo que se convierte</span><span class="sxs-lookup"><span data-stu-id="03680-105">What Is Converted</span></span>

<span data-ttu-id="03680-106">Durante la conversión, la utilidad MTSTOCOM convierte los roles, las asignaciones de roles, las interfaces, los métodos, los usuarios, la lista de equipos y la mayor parte de la configuración del equipo.</span><span class="sxs-lookup"><span data-stu-id="03680-106">During conversion, the MTSTOCOM utility converts roles, role assignments, interfaces, methods, users, the computer list, and most computer settings.</span></span> <span data-ttu-id="03680-107">La utilidad MTSTOCOM también convierte la identidad y la contraseña para un paquete MTS.</span><span class="sxs-lookup"><span data-stu-id="03680-107">The MTSTOCOM utility also converts the identity and password for an MTS package.</span></span>

<span data-ttu-id="03680-108">Los nuevos atributos COM+ que no estaban disponibles en MTS se establecen automáticamente en los siguientes valores predeterminados para todos los componentes de MTS convertidos.</span><span class="sxs-lookup"><span data-stu-id="03680-108">The new COM+ attributes that were not available in MTS are automatically set to the following defaults for all converted MTS components.</span></span> <span data-ttu-id="03680-109">Estos valores predeterminados se pueden cambiar mediante la herramienta administrativa Servicios de componentes o las interfaces administrativas de COM+.</span><span class="sxs-lookup"><span data-stu-id="03680-109">These defaults can be changed using either the Component Services administrative tool or the COM+ administrative interfaces.</span></span>

-   <span data-ttu-id="03680-110">Activación JIT habilitada.</span><span class="sxs-lookup"><span data-stu-id="03680-110">JIT activation enabled.</span></span>
-   <span data-ttu-id="03680-111">Agrupación de objetos deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="03680-111">Object pooling disabled.</span></span>
-   <span data-ttu-id="03680-112">La sincronización es igual que la configuración de la transacción.</span><span class="sxs-lookup"><span data-stu-id="03680-112">Synchronization same as Transaction setting.</span></span>

## <a name="conversion-issues"></a><span data-ttu-id="03680-113">Problemas de conversión</span><span class="sxs-lookup"><span data-stu-id="03680-113">Conversion Issues</span></span>

<span data-ttu-id="03680-114">COM+ se instala automáticamente al instalar Windows.</span><span class="sxs-lookup"><span data-stu-id="03680-114">COM+ is automatically installed when you install Windows.</span></span> <span data-ttu-id="03680-115">No es posible desinstalar COM+.</span><span class="sxs-lookup"><span data-stu-id="03680-115">It is not possible to uninstall COM+.</span></span> <span data-ttu-id="03680-116">Entre los problemas relacionados con las actualizaciones de las instalaciones de MTS y COM+ existentes se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="03680-116">Issues related to upgrades of existing MTS and COM+ installations include the following:</span></span>

-   <span data-ttu-id="03680-117">Si actualmente usa MTS 1,0, MTS se actualiza automáticamente a COM+.</span><span class="sxs-lookup"><span data-stu-id="03680-117">If you are currently using MTS 1.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="03680-118">Sin embargo, los paquetes definidos por el usuario se perderán y deberá volver a crearlos.</span><span class="sxs-lookup"><span data-stu-id="03680-118">However, user-defined packages will be lost and you must re-create them.</span></span>
-   <span data-ttu-id="03680-119">Si actualmente usa MTS 2,0, MTS se actualiza automáticamente a COM+.</span><span class="sxs-lookup"><span data-stu-id="03680-119">If you are currently using MTS 2.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="03680-120">Todos los paquetes definidos por el usuario se actualizarán a las aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="03680-120">All user-defined packages will be upgraded to COM+ applications.</span></span> <span data-ttu-id="03680-121">Todos los componentes deben funcionar tal y como se encontraban en MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="03680-121">All components should work as they did under MTS 2.0.</span></span>
-   <span data-ttu-id="03680-122">Si usa MTS 1,0 y MTS 2,0 y ha instalado la opción SDK, se quitarán los archivos del SDK.</span><span class="sxs-lookup"><span data-stu-id="03680-122">If you are using MTS 1.0 and MTS 2.0 and have installed the SDK option, the SDK files will be removed.</span></span> <span data-ttu-id="03680-123">Puede instalar el SDK de COM+ más reciente a través de la Microsoft Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="03680-123">You can install the latest COM+ SDK through the Microsoft Windows SDK.</span></span>
-   <span data-ttu-id="03680-124">No se puede administrar un equipo MTS remoto desde un equipo de COM+.</span><span class="sxs-lookup"><span data-stu-id="03680-124">You cannot manage a remote MTS computer from a COM+ computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03680-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03680-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03680-126">Conversión automática desde MTS</span><span class="sxs-lookup"><span data-stu-id="03680-126">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="03680-127">Conversión manual desde MTS</span><span class="sxs-lookup"><span data-stu-id="03680-127">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="03680-128">Biblioteca de administración de MTS</span><span class="sxs-lookup"><span data-stu-id="03680-128">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



