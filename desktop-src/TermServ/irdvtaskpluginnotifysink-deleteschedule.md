---
title: IRDVTaskPluginNotifySink DeleteSchedule, método
description: El agente de tareas lo llama para eliminar una tarea programada.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- Método DeleteSchedule Servicios de Escritorio remoto
- Método DeleteSchedule Servicios de Escritorio remoto, interfaz IRDVTaskPluginNotifySink
- Interfaz IRDVTaskPluginNotifySink Servicios de Escritorio remoto, método DeleteSchedule
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f00bcc740f87acb7f051decd5f2fc9b55ffbf642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151115"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a><span data-ttu-id="b5055-106">IRDVTaskPluginNotifySink::D método eleteSchedule</span><span class="sxs-lookup"><span data-stu-id="b5055-106">IRDVTaskPluginNotifySink::DeleteSchedule method</span></span>

<span data-ttu-id="b5055-107">El agente de tareas lo llama para eliminar una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="b5055-107">Called by the task agent to delete a scheduled task.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5055-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5055-108">Syntax</span></span>


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a><span data-ttu-id="b5055-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5055-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5055-110">*bstrIdentifier* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5055-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5055-111">El identificador de la tarea programada.</span><span class="sxs-lookup"><span data-stu-id="b5055-111">The identifier of the scheduled task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5055-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5055-112">Return value</span></span>

<span data-ttu-id="b5055-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b5055-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5055-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5055-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5055-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5055-115">Requirements</span></span>



| <span data-ttu-id="b5055-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5055-116">Requirement</span></span> | <span data-ttu-id="b5055-117">Value</span><span class="sxs-lookup"><span data-stu-id="b5055-117">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b5055-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5055-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b5055-119">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="b5055-119">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="b5055-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5055-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b5055-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5055-121">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5055-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5055-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5055-123">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="b5055-123">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





