---
description: La acción SelfUnregModules anula el registro de todos los módulos enumerados en la tabla SelfReg que están programados para desinstalarse. El instalador no se registra automáticamente. Archivos EXE.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Acción SelfUnregModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653051"
---
# <a name="selfunregmodules-action"></a><span data-ttu-id="cc0fe-104">Acción SelfUnregModules</span><span class="sxs-lookup"><span data-stu-id="cc0fe-104">SelfUnregModules Action</span></span>

<span data-ttu-id="cc0fe-105">La acción SelfUnregModules anula el registro de todos los módulos enumerados en la [tabla SelfReg](selfreg-table.md) que están programados para desinstalarse.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-105">The SelfUnregModules action unregisters all modules listed in the [SelfReg table](selfreg-table.md) that are scheduled to be uninstalled.</span></span> <span data-ttu-id="cc0fe-106">El instalador no se registra automáticamente. Archivos EXE.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-106">The installer does not self-register .EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cc0fe-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="cc0fe-107">Sequence Restrictions</span></span>

<span data-ttu-id="cc0fe-108">La acción [InstallValidate](installvalidate-action.md) debe aparecer antes de la acción SelfUnregModules en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-108">The [InstallValidate](installvalidate-action.md) action must appear before the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="cc0fe-109">Si se usa una acción [SelfRegModules](selfregmodules-action.md) , debe aparecer después de la acción SelfUnregModules en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-109">If a [SelfRegModules](selfregmodules-action.md) action is used it must appear after the SelfUnregModules action in the sequence.</span></span> <span data-ttu-id="cc0fe-110">Si se usa una [acción RemoveFiles](removefiles-action.md) , debe aparecer después de la acción SelfUnregModules en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-110">If a [RemoveFiles action](removefiles-action.md) is used it must appear after the SelfUnregModules action in the sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cc0fe-111">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="cc0fe-111">ActionData Messages</span></span>



| <span data-ttu-id="cc0fe-112">Campo</span><span class="sxs-lookup"><span data-stu-id="cc0fe-112">Field</span></span> | <span data-ttu-id="cc0fe-113">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="cc0fe-113">Description of action data</span></span>                             |
|-------|--------------------------------------------------------|
| <span data-ttu-id="cc0fe-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="cc0fe-114">\[1\]</span></span> | <span data-ttu-id="cc0fe-115">Identificador del archivo de módulo no registrado.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-115">Identifier of unregistered module file.</span></span>                |
| <span data-ttu-id="cc0fe-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="cc0fe-116">\[2\]</span></span> | <span data-ttu-id="cc0fe-117">Identificador de la carpeta que contiene el archivo de módulo no registrado.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-117">Identifier of folder holding unregistered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cc0fe-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc0fe-118">Remarks</span></span>

<span data-ttu-id="cc0fe-119">La acción SelfUnregModules intenta llamar a la función [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) del módulo cuyo registro se va a anular.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-119">The SelfUnregModules action attempts to call the [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) function of the module that is to be unregistered.</span></span> <span data-ttu-id="cc0fe-120">Esta acción se ejecuta con privilegios elevados cuando la instalación se ejecuta con privilegios elevados, como durante una instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="cc0fe-121">Durante una instalación por usuario, el instalador ejecuta esta acción con privilegios de usuario.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-121">During a per-user installation, the installer runs this action with user privileges.</span></span>

<span data-ttu-id="cc0fe-122">Tenga en cuenta que no puede especificar el orden en el que el instalador anula el registro de los archivos dll de registro automático mediante la acción SelfUnRegModules.</span><span class="sxs-lookup"><span data-stu-id="cc0fe-122">Note that you cannot specify the order in which the installer unregisters self-registering DLLs by using the SelfUnRegModules action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc0fe-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc0fe-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc0fe-124">Especificar el orden de registro automático</span><span class="sxs-lookup"><span data-stu-id="cc0fe-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
