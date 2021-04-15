---
title: IRDVTaskPlugin Initialize (método)
description: Se llama para inicializar el agente de tareas.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Método Initialize Servicios de Escritorio remoto
- Método Initialize Servicios de Escritorio remoto, interfaz IRDVTaskPlugin
- Interfaz IRDVTaskPlugin Servicios de Escritorio remoto, método Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422062"
---
# <a name="irdvtaskplugininitialize-method"></a><span data-ttu-id="a7bc9-106">IRDVTaskPlugin:: Initialize (método)</span><span class="sxs-lookup"><span data-stu-id="a7bc9-106">IRDVTaskPlugin::Initialize method</span></span>

<span data-ttu-id="a7bc9-107">Se llama para inicializar el agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="a7bc9-107">Called to initialize the task agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7bc9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7bc9-108">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a><span data-ttu-id="a7bc9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7bc9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7bc9-110">*pNotifySink* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7bc9-110">*pNotifySink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7bc9-111">Tipo: \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) \** _</span><span class="sxs-lookup"><span data-stu-id="a7bc9-111">Type: \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\** _</span></span>

<span data-ttu-id="a7bc9-112">Un puntero a una interfaz [_ *IRDVTaskPluginNotifySink* \*](irdvtaskpluginnotifysink.md) que el agente de tareas usa para comunicarse con el agente de desencadenador.</span><span class="sxs-lookup"><span data-stu-id="a7bc9-112">A pointer to an [_ *IRDVTaskPluginNotifySink*\*](irdvtaskpluginnotifysink.md) interface that the task agent uses to communicate with the trigger agent.</span></span> <span data-ttu-id="a7bc9-113">Debe liberar esta interfaz cuando ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="a7bc9-113">You must release this interface when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7bc9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7bc9-114">Return value</span></span>

<span data-ttu-id="a7bc9-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a7bc9-115">Type: **HRESULT**</span></span>

<span data-ttu-id="a7bc9-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a7bc9-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7bc9-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7bc9-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7bc9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7bc9-118">Requirements</span></span>



| <span data-ttu-id="a7bc9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7bc9-119">Requirement</span></span> | <span data-ttu-id="a7bc9-120">Value</span><span class="sxs-lookup"><span data-stu-id="a7bc9-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="a7bc9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7bc9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a7bc9-122">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="a7bc9-122">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="a7bc9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7bc9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a7bc9-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7bc9-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7bc9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7bc9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7bc9-126">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="a7bc9-126">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





