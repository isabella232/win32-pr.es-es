---
title: IRDVTaskPluginNotifySink OnTaskStateChange, método
description: Se usa para notificar al agente de desencadenador que el estado de una tarea ha cambiado.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Método OnTaskStateChange Servicios de Escritorio remoto
- Método OnTaskStateChange Servicios de Escritorio remoto, interfaz IRDVTaskPluginNotifySink
- Interfaz IRDVTaskPluginNotifySink Servicios de Escritorio remoto, método OnTaskStateChange
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676957"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a><span data-ttu-id="5d2c7-106">IRDVTaskPluginNotifySink:: OnTaskStateChange (método)</span><span class="sxs-lookup"><span data-stu-id="5d2c7-106">IRDVTaskPluginNotifySink::OnTaskStateChange method</span></span>

<span data-ttu-id="5d2c7-107">Se usa para notificar al agente de desencadenador que el estado de una tarea ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="5d2c7-107">Used to notify the trigger agent that the state of a task has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2c7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d2c7-108">Syntax</span></span>


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a><span data-ttu-id="5d2c7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d2c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d2c7-110">*bstrIdentifier* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d2c7-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2c7-111">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5d2c7-111">Type: **BSTR**</span></span>

<span data-ttu-id="5d2c7-112">Identificador único de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5d2c7-112">The identifier of the task.</span></span> <span data-ttu-id="5d2c7-113">Este es el identificador que se pasa al método [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2c7-113">This is the identifier passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="5d2c7-114">*Estado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5d2c7-114">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2c7-115">Tipo: estado de la **[ **\_ tarea \_ RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span><span class="sxs-lookup"><span data-stu-id="5d2c7-115">Type: **[**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span></span>

<span data-ttu-id="5d2c7-116">Un valor de la enumeración del [**\_ \_ Estado de la tarea RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que especifica el nuevo estado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5d2c7-116">A value of the [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration that specifies the new state of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d2c7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d2c7-117">Return value</span></span>

<span data-ttu-id="5d2c7-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5d2c7-118">Type: **HRESULT**</span></span>

<span data-ttu-id="5d2c7-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5d2c7-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d2c7-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d2c7-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2c7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d2c7-121">Requirements</span></span>



| <span data-ttu-id="5d2c7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d2c7-122">Requirement</span></span> | <span data-ttu-id="5d2c7-123">Value</span><span class="sxs-lookup"><span data-stu-id="5d2c7-123">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="5d2c7-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d2c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d2c7-125">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="5d2c7-125">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="5d2c7-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d2c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d2c7-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d2c7-127">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d2c7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d2c7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2c7-129">**Estado de la \_ tarea RDV \_**</span><span class="sxs-lookup"><span data-stu-id="5d2c7-129">**RDV\_TASK\_STATUS**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[<span data-ttu-id="5d2c7-130">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="5d2c7-130">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





