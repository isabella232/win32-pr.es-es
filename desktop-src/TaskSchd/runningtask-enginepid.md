---
title: Propiedad RunningTask. EnginePID
description: En el caso de scripting, obtiene el identificador de proceso del motor (proceso) que está ejecutando la tarea.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Programador de tareas de la propiedad EnginePID
- Programador de tareas de la propiedad EnginePID, objeto RunningTask
- Programador de tareas de objeto RunningTask, propiedad EnginePID
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676830"
---
# <a name="runningtaskenginepid-property"></a><span data-ttu-id="af35b-106">Propiedad RunningTask. EnginePID</span><span class="sxs-lookup"><span data-stu-id="af35b-106">RunningTask.EnginePID property</span></span>

<span data-ttu-id="af35b-107">En el caso de scripting, obtiene el identificador de proceso del motor (proceso) que está ejecutando la tarea.</span><span class="sxs-lookup"><span data-stu-id="af35b-107">For scripting, gets the process ID for the engine (process) which is running the task.</span></span>

<span data-ttu-id="af35b-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af35b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="af35b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af35b-109">Syntax</span></span>


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a><span data-ttu-id="af35b-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="af35b-110">Property value</span></span>

<span data-ttu-id="af35b-111">IDENTIFICADOR de proceso del motor que ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="af35b-111">The process ID for the engine which is running the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="af35b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af35b-112">Remarks</span></span>

<span data-ttu-id="af35b-113">El ID. de proceso devuelto por esta propiedad no se puede anexar directamente a una cadena.</span><span class="sxs-lookup"><span data-stu-id="af35b-113">The process ID returned by this property cannot be appended directly to a string.</span></span> <span data-ttu-id="af35b-114">El valor devuelto debe convertirse primero en un valor entero mediante una llamada a la función [cint](/previous-versions//fctcwhw9(v=vs.85)) en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="af35b-114">The returned value needs to be converted to an integer value first by calling the [CInt](/previous-versions//fctcwhw9(v=vs.85)) function on the returned value.</span></span>


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a><span data-ttu-id="af35b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af35b-115">Requirements</span></span>



| <span data-ttu-id="af35b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af35b-116">Requirement</span></span> | <span data-ttu-id="af35b-117">Value</span><span class="sxs-lookup"><span data-stu-id="af35b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af35b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af35b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af35b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="af35b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="af35b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af35b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af35b-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="af35b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af35b-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="af35b-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="af35b-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af35b-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af35b-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="af35b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af35b-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af35b-125"><dt>Taskschd.dll</dt></span></span> </dl> |



 

