---
description: La acción SelfRegModules procesa todos los módulos enumerados en la tabla SelfReg y registra todos los módulos instalados en el sistema. El instalador no registra automáticamente los archivos EXE.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Acción SelfRegModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75895b1886fad51f36113ce6e677ba6a534ab0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669837"
---
# <a name="selfregmodules-action"></a><span data-ttu-id="6eabb-104">Acción SelfRegModules</span><span class="sxs-lookup"><span data-stu-id="6eabb-104">SelfRegModules Action</span></span>

<span data-ttu-id="6eabb-105">La acción SelfRegModules procesa todos los módulos enumerados en la tabla [SelfReg](selfreg-table.md) y registra todos los módulos instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="6eabb-105">The SelfRegModules action processes all modules listed in the [SelfReg](selfreg-table.md) table and registers all installed modules with the system.</span></span> <span data-ttu-id="6eabb-106">El instalador no registra automáticamente los archivos EXE.</span><span class="sxs-lookup"><span data-stu-id="6eabb-106">The installer does not self-register EXE files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6eabb-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="6eabb-107">Sequence Restrictions</span></span>

<span data-ttu-id="6eabb-108">Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de llamar a la acción SelfRegModules.</span><span class="sxs-lookup"><span data-stu-id="6eabb-108">The [InstallValidate](installvalidate-action.md) action must be called before calling the SelfRegModules action.</span></span> <span data-ttu-id="6eabb-109">Si se utiliza una acción [InstallFiles](installfiles-action.md) , debe aparecer antes de la acción SelfRegModules en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6eabb-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear before the SelfRegModules action in the sequence.</span></span> <span data-ttu-id="6eabb-110">Dado que la acción SelfRegModules cambia el sistema, SelfRegModules debe aparecer después de la [acción InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="6eabb-110">Because the SelfRegModules action changes the system, SelfRegModules should come after the [InstallInitialize action](installinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6eabb-111">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="6eabb-111">ActionData Messages</span></span>



| <span data-ttu-id="6eabb-112">Campo</span><span class="sxs-lookup"><span data-stu-id="6eabb-112">Field</span></span> | <span data-ttu-id="6eabb-113">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="6eabb-113">Description of action data</span></span>                           |
|-------|------------------------------------------------------|
| <span data-ttu-id="6eabb-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="6eabb-114">\[1\]</span></span> | <span data-ttu-id="6eabb-115">Identificador del archivo de módulo registrado.</span><span class="sxs-lookup"><span data-stu-id="6eabb-115">Identifier of registered module file.</span></span>                |
| <span data-ttu-id="6eabb-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="6eabb-116">\[2\]</span></span> | <span data-ttu-id="6eabb-117">Identificador de la carpeta que contiene el archivo de módulo registrado.</span><span class="sxs-lookup"><span data-stu-id="6eabb-117">Identifier of folder holding registered module file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6eabb-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6eabb-118">Remarks</span></span>

<span data-ttu-id="6eabb-119">La acción SelfRegModules intenta llamar a la función [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) del módulo programado para su registro.</span><span class="sxs-lookup"><span data-stu-id="6eabb-119">The SelfRegModules action attempts to call the [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function of the module scheduled to be registered.</span></span> <span data-ttu-id="6eabb-120">Esta acción se ejecuta con privilegios elevados cuando la instalación se ejecuta con privilegios elevados, como durante una instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="6eabb-120">This action runs with elevated privileges when the installation is being run with elevated privileges, such as during a per-machine installation.</span></span> <span data-ttu-id="6eabb-121">Durante una instalación por usuario, el instalador ejecuta esta acción con privilegios de usuario.</span><span class="sxs-lookup"><span data-stu-id="6eabb-121">During a per-user installation the installer runs this action with user privileges.</span></span>

<span data-ttu-id="6eabb-122">Tenga en cuenta que no puede especificar el orden en el que el instalador registra los archivos dll de registro automático mediante la [acción SelfUnRegModules](selfunregmodules-action.md).</span><span class="sxs-lookup"><span data-stu-id="6eabb-122">Note that you cannot specify the order in which the installer registers self-registering DLLs by using the [SelfUnRegModules action](selfunregmodules-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6eabb-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6eabb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eabb-124">Especificar el orden de registro automático</span><span class="sxs-lookup"><span data-stu-id="6eabb-124">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
