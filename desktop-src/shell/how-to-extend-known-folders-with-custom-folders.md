---
description: Los fabricantes de software independientes (ISV) pueden extender el conjunto de carpetas conocidas en un sistema mediante el registro de carpetas conocidas propias.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Cómo extender carpetas conocidas con carpetas personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276748"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a><span data-ttu-id="ba5ef-103">Cómo extender carpetas conocidas con carpetas personalizadas</span><span class="sxs-lookup"><span data-stu-id="ba5ef-103">How to Extend Known Folders with Custom Folders</span></span>

<span data-ttu-id="ba5ef-104">Los fabricantes de software independientes (ISV) pueden extender el conjunto de carpetas conocidas en un sistema mediante el registro de carpetas conocidas propias.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-104">Independent software vendors (ISVs) can extend the set of known folders on a system by registering known folders of their own.</span></span> <span data-ttu-id="ba5ef-105">Una vez registrada, el sistema conoce esas carpetas de terceros.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-105">Once registered, those third-party folders are known to the system.</span></span> <span data-ttu-id="ba5ef-106">Los encuentra cualquier llamada a [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span><span class="sxs-lookup"><span data-stu-id="ba5ef-106">They are found by any call to [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span></span> <span data-ttu-id="ba5ef-107">Tenga en cuenta que una carpeta conocida debe ser una carpeta por equipo.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-107">Note that a known folder must be a per-machine folder.</span></span> <span data-ttu-id="ba5ef-108">No se puede crear una carpeta conocida por usuario.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-108">You cannot create a per-user known folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="ba5ef-109">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ba5ef-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="ba5ef-110">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="ba5ef-110">Step 1:</span></span>

<span data-ttu-id="ba5ef-111">Defina la carpeta conocida a través de una estructura de [**\_ definición de KNOWNFOLDER**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) .</span><span class="sxs-lookup"><span data-stu-id="ba5ef-111">Define your known folder through a [**KNOWNFOLDER\_DEFINITION**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) structure.</span></span>

### <a name="step-2"></a><span data-ttu-id="ba5ef-112">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="ba5ef-112">Step 2:</span></span>

<span data-ttu-id="ba5ef-113">Registre la carpeta conocida a través de una llamada a [**IKnownFolderManager:: RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span><span class="sxs-lookup"><span data-stu-id="ba5ef-113">Register the known folder through a call to [**IKnownFolderManager::RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba5ef-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba5ef-114">Remarks</span></span>

<span data-ttu-id="ba5ef-115">Si crea una carpeta conocida para la aplicación como parte del procedimiento de instalación, también debe incluir [**IKnownFolderManager:: UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) como parte del código de desinstalación.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-115">If you create a known folder for your application as part of your installation procedure, you must also include [**IKnownFolderManager::UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) as part of your uninstallation code.</span></span>

<span data-ttu-id="ba5ef-116">Tenga en cuenta el motivo por el que desea que la carpeta se incluya en el sistema de carpetas conocidas antes de registrarla.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-116">Give consideration to why you want your folder to be included in the known folder system before you register it.</span></span> <span data-ttu-id="ba5ef-117">Debe tener un motivo válido para elevar la carpeta a ese nivel de visibilidad del sistema.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-117">You should have a valid reason for elevating your folder to that level of system visibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba5ef-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba5ef-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ba5ef-119">[Ejemplo de carpetas conocidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba5ef-119">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
