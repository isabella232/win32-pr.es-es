---
title: IRDVTaskPlugin StartTask, método
description: Se llama para iniciar la tarea de actualización en la máquina virtual.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Método StartTask Servicios de Escritorio remoto
- Método StartTask Servicios de Escritorio remoto, interfaz IRDVTaskPlugin
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto, método StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491320"
---
# <a name="irdvtaskpluginstarttask-method"></a><span data-ttu-id="6387c-106">IRDVTaskPlugin:: StartTask (método)</span><span class="sxs-lookup"><span data-stu-id="6387c-106">IRDVTaskPlugin::StartTask method</span></span>

<span data-ttu-id="6387c-107">Se llama para iniciar la tarea de actualización en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6387c-107">Called to start the update task on the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6387c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6387c-108">Syntax</span></span>


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a><span data-ttu-id="6387c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6387c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6387c-110">*Etiqueta* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6387c-110">*Label* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6387c-111">Etiqueta de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6387c-111">The label for the task.</span></span> <span data-ttu-id="6387c-112">Esta es la etiqueta que se pasó al agente de desencadenador en el método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="6387c-112">This is the label that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="6387c-113">*Identificador de* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6387c-113">*Identifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6387c-114">Identificador único de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6387c-114">The identifier of the task.</span></span> <span data-ttu-id="6387c-115">Este es el identificador que se pasó al agente de desencadenador en el método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="6387c-115">This is the identifier that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="6387c-116">*Contexto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6387c-116">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6387c-117">Datos opcionales para la tarea.</span><span class="sxs-lookup"><span data-stu-id="6387c-117">Optional data for the task.</span></span> <span data-ttu-id="6387c-118">Estos son los datos que se pasaron al agente de desencadenador en el método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="6387c-118">This is the data that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6387c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6387c-119">Return value</span></span>

<span data-ttu-id="6387c-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6387c-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6387c-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6387c-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6387c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6387c-122">Requirements</span></span>



| <span data-ttu-id="6387c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6387c-123">Requirement</span></span> | <span data-ttu-id="6387c-124">Value</span><span class="sxs-lookup"><span data-stu-id="6387c-124">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="6387c-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6387c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6387c-126">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="6387c-126">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="6387c-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6387c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6387c-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6387c-128">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6387c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6387c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6387c-130">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="6387c-130">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





