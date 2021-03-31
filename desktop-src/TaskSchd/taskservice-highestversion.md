---
title: Propiedad TaskService. HighestVersion
description: En scripting, indica la versión más alta de Programador de tareas que admite un equipo.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Programador de tareas de la propiedad HighestVersion
- Programador de tareas de la propiedad HighestVersion, objeto TaskService
- Programador de tareas de objeto TaskService, propiedad HighestVersion
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803950"
---
# <a name="taskservicehighestversion-property"></a><span data-ttu-id="3c26d-106">Propiedad TaskService. HighestVersion</span><span class="sxs-lookup"><span data-stu-id="3c26d-106">TaskService.HighestVersion property</span></span>

<span data-ttu-id="3c26d-107">En scripting, indica la versión más alta de Programador de tareas que admite un equipo.</span><span class="sxs-lookup"><span data-stu-id="3c26d-107">For scripting, indicates the highest version of Task Scheduler that a computer supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c26d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c26d-108">Syntax</span></span>


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a><span data-ttu-id="3c26d-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3c26d-109">Property value</span></span>

<span data-ttu-id="3c26d-110">La versión más alta de Programador de tareas que admite un equipo.</span><span class="sxs-lookup"><span data-stu-id="3c26d-110">The highest version of Task Scheduler that a computer supports.</span></span> <span data-ttu-id="3c26d-111">La versión más alta es un valor que se divide en MajorVersion/MinorVersion en el límite de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="3c26d-111">The highest version is a value that is split into MajorVersion/MinorVersion on the 16-bit boundary.</span></span> <span data-ttu-id="3c26d-112">El servicio Programador de tareas devuelve 1 para la versión principal y 2 para la versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="3c26d-112">The Task Scheduler service returns 1 for the major version and 2 for the minor version.</span></span> <span data-ttu-id="3c26d-113">Utilice la función [CLng](/previous-versions//ck4c5842(v=vs.85)) para obtener el valor entero de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3c26d-113">Use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the integer value of the property.</span></span>

## <a name="examples"></a><span data-ttu-id="3c26d-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3c26d-114">Examples</span></span>

<span data-ttu-id="3c26d-115">En el código siguiente se muestra cómo usar la función [CLng](/previous-versions//ck4c5842(v=vs.85)) para obtener el valor de la propiedad **HighestVersion** .</span><span class="sxs-lookup"><span data-stu-id="3c26d-115">The following code shows how to use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the value of the **HighestVersion** property.</span></span>


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a><span data-ttu-id="3c26d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c26d-116">Requirements</span></span>



| <span data-ttu-id="3c26d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c26d-117">Requirement</span></span> | <span data-ttu-id="3c26d-118">Value</span><span class="sxs-lookup"><span data-stu-id="3c26d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c26d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c26d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c26d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3c26d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3c26d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c26d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c26d-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c26d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c26d-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3c26d-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="3c26d-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3c26d-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3c26d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c26d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c26d-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c26d-126"><dt>Taskschd.dll</dt></span></span> </dl> |



 

