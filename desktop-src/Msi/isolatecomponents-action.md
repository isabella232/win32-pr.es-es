---
description: La acción IsolateComponents instala una copia de un componente (normalmente una DLL compartida) en una ubicación privada para su uso por parte de una aplicación específica (normalmente un archivo. exe).
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Acción IsolateComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361395"
---
# <a name="isolatecomponents-action"></a><span data-ttu-id="1745b-103">Acción IsolateComponents</span><span class="sxs-lookup"><span data-stu-id="1745b-103">IsolateComponents Action</span></span>

<span data-ttu-id="1745b-104">La acción IsolateComponents instala una copia de un componente (normalmente una DLL compartida) en una ubicación privada para su uso por parte de una aplicación específica (normalmente un archivo. exe).</span><span class="sxs-lookup"><span data-stu-id="1745b-104">The IsolateComponents action installs a copy of a component (commonly a shared DLL) into a private location for use by a specific application (typically an .exe).</span></span> <span data-ttu-id="1745b-105">Esto aísla la aplicación de otras copias del componente que se puede instalar en una ubicación compartida del equipo.</span><span class="sxs-lookup"><span data-stu-id="1745b-105">This isolates the application from other copies of the component that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="1745b-106">Para obtener más información, vea [componentes aislados](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="1745b-106">For more information, see [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="1745b-107">La acción hace referencia a cada registro de la [tabla IsolatedComponent](isolatedcomponent-table.md) y asocia los archivos del componente enumerados en el \_ campo compartido componente con el componente que aparece en el \_ campo aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="1745b-107">The action refers to each record of the [IsolatedComponent table](isolatedcomponent-table.md) and associates the files of the component listed in the Component\_Shared field with the component listed in the Component\_Application field.</span></span> <span data-ttu-id="1745b-108">El instalador instala los archivos de componentes \_ compartidos en el mismo directorio que la aplicación de componentes \_ .</span><span class="sxs-lookup"><span data-stu-id="1745b-108">The installer installs the files of Component\_Shared into the same directory as Component\_Application.</span></span> <span data-ttu-id="1745b-109">El instalador genera un archivo en este directorio, de cero bytes de longitud y tiene el nombre de archivo corto del archivo de clave de la aplicación de componentes \_ (normalmente, es el mismo nombre de archivo que el. exe) anexado con. local.</span><span class="sxs-lookup"><span data-stu-id="1745b-109">The installer generates a file in this directory, zero bytes in length, having the short filename name of the key file for Component\_Application (typically this is the same file name as the .exe) appended with .local.</span></span> <span data-ttu-id="1745b-110">La acción IsolatedComponent no afecta a la instalación de la \_ aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="1745b-110">The IsolatedComponent action does not affect the installation of Component\_Application.</span></span> <span data-ttu-id="1745b-111">Al desinstalar \_ la aplicación de componentes, también se quitan los \_ archivos compartidos del componente y el archivo. local del directorio.</span><span class="sxs-lookup"><span data-stu-id="1745b-111">Uninstalling Component\_Application also removes the Component\_Shared files and the .local file from the directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1745b-112">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="1745b-112">Sequence Restrictions</span></span>

<span data-ttu-id="1745b-113">La acción IsolateComponents solo se puede usar en la [tabla InstallUISequence](installuisequence-table.md) y en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1745b-113">The IsolateComponents action can be used only in the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="1745b-114">Esta acción debe aparecer después de la [acción CostInitialize](costinitialize-action.md) y antes de la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="1745b-114">This action must come after the [CostInitialize action](costinitialize-action.md) and before the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1745b-115">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="1745b-115">ActionData Messages</span></span>

<span data-ttu-id="1745b-116">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="1745b-116">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="1745b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1745b-117">Remarks</span></span>

<span data-ttu-id="1745b-118">Si la columna condición de la acción IsolateComponents se evalúa como true o se deja en blanco, el instalador aísla todos los componentes enumerados en la [tabla IsolatedComponent](isolatedcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="1745b-118">If the Condition column for the IsolateComponents action evaluates to True, or is left blank, the installer isolates all the components listed in the [IsolatedComponent table](isolatedcomponent-table.md).</span></span> <span data-ttu-id="1745b-119">Si la columna condition se evalúa como false, el instalador omite la tabla IsolatedComponent y comparte los componentes de forma habitual.</span><span class="sxs-lookup"><span data-stu-id="1745b-119">If the Condition column evaluates to False, the installer ignores the IsolatedComponent table and shares the components usual.</span></span> <span data-ttu-id="1745b-120">La propiedad [**RedirectedDllSupport**](redirecteddllsupport.md) se puede usar para condicionar esta acción.</span><span class="sxs-lookup"><span data-stu-id="1745b-120">The [**RedirectedDllSupport**](redirecteddllsupport.md) property may be used to condition this action.</span></span> <span data-ttu-id="1745b-121">Para obtener más información, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1745b-121">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



