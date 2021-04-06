---
description: La acción ADMIN es una acción de nivel superior que se usa para realizar instalaciones administrativas.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Acción de administración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909126"
---
# <a name="admin-action"></a><span data-ttu-id="17394-103">Acción de administración</span><span class="sxs-lookup"><span data-stu-id="17394-103">ADMIN Action</span></span>

<span data-ttu-id="17394-104">La acción ADMIN es una acción de nivel superior que se usa para realizar [instalaciones administrativas](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="17394-104">The ADMIN action is a top-level action used to perform [administrative installations](administrative-installation.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="17394-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="17394-105">Sequence Restrictions</span></span>

<span data-ttu-id="17394-106">No hay restricciones de secuencia.</span><span class="sxs-lookup"><span data-stu-id="17394-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="17394-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="17394-107">ActionData Messages</span></span>

<span data-ttu-id="17394-108">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="17394-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="17394-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17394-109">Remarks</span></span>

<span data-ttu-id="17394-110">No se llama a la acción ADMIN desde la secuencia de la tabla de acciones, Windows Installer ejecuta esta acción cuando se llama a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) con el parámetro *szCommandLine* establecido en "Action = admin" o se llama al Msiexec.exe ejecutable de la línea de comandos con el modificador de la línea de comandos '/a '.</span><span class="sxs-lookup"><span data-stu-id="17394-110">The ADMIN action is not called from within the action table sequence, Windows Installer executes this action when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to "ACTION=ADMIN" or the command line executable Msiexec.exe is called with the '/a' command line switch.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17394-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17394-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17394-112">Tabla AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="17394-112">AdminUISequence Table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="17394-113">Tabla AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="17394-113">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)
</dt> </dl>

 

 



