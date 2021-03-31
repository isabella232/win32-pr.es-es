---
description: La acción de instalación es una acción de nivel superior llamada para instalar o quitar componentes.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Acción de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082486"
---
# <a name="install-action"></a><span data-ttu-id="f69a1-103">Acción de instalación</span><span class="sxs-lookup"><span data-stu-id="f69a1-103">INSTALL Action</span></span>

<span data-ttu-id="f69a1-104">La acción de instalación es una acción de nivel superior llamada para instalar o quitar componentes.</span><span class="sxs-lookup"><span data-stu-id="f69a1-104">The INSTALL action is a top-level action called to install or remove components.</span></span> <span data-ttu-id="f69a1-105">Esta acción consulta la [tabla InstallUISequence](installuisequence-table.md) y la [tabla InstallExecuteSequence](installexecutesequence-table.md) para la acción que se va a ejecutar, la condición para la ejecución de la acción y el lugar de la acción en la secuencia:</span><span class="sxs-lookup"><span data-stu-id="f69a1-105">This action queries the [InstallUISequence Table](installuisequence-table.md) and [InstallExecuteSequence Table](installexecutesequence-table.md) for the action to execute, the condition for action execution, and the place of the action in the sequence:</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f69a1-106">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="f69a1-106">Sequence Restrictions</span></span>

<span data-ttu-id="f69a1-107">No hay restricciones de secuencia.</span><span class="sxs-lookup"><span data-stu-id="f69a1-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f69a1-108">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="f69a1-108">ActionData Messages</span></span>

<span data-ttu-id="f69a1-109">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="f69a1-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="f69a1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f69a1-110">Remarks</span></span>

<span data-ttu-id="f69a1-111">No se llama a la acción de instalación desde dentro de la secuencia de la tabla de acciones, se pasa a Windows Installer cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) , o se llama al Msiexec.exe ejecutable de línea de comandos con el modificador de línea de comandos '**/i**', o cuando se llama a cualquier función de instalador que puede realizar una tarea de instalación, como [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)o [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="f69a1-111">The INSTALL action is not called from within the action table sequence, it is passed to Windows Installer when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called, or the command line executable Msiexec.exe is called with the '**/i**' command line switch, or when any installer function is called that may perform an installation task, such as [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta), or [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span>

 

 



