---
title: IRDVTaskPlugin Terminate (método)
description: Se llama cuando se está cerrando el agente de tareas.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Método Terminate Servicios de Escritorio remoto
- Método Terminate Servicios de Escritorio remoto, interfaz IRDVTaskPlugin
- Servicios de Escritorio remoto de la interfaz IRDVTaskPlugin, método Terminate
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422420"
---
# <a name="irdvtaskpluginterminate-method"></a><span data-ttu-id="7cf5c-106">IRDVTaskPlugin:: Terminate (método)</span><span class="sxs-lookup"><span data-stu-id="7cf5c-106">IRDVTaskPlugin::Terminate method</span></span>

<span data-ttu-id="7cf5c-107">Se llama cuando se está cerrando el agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="7cf5c-107">Called when the task agent is being shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf5c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cf5c-108">Syntax</span></span>


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="7cf5c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7cf5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf5c-110">*HR* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7cf5c-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf5c-111">Indica si el apagado se debe a un apagado normal o a un error.</span><span class="sxs-lookup"><span data-stu-id="7cf5c-111">Indicates whether the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="7cf5c-112">Si el apagado es normal, contiene **S \_ correctos**.</span><span class="sxs-lookup"><span data-stu-id="7cf5c-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="7cf5c-113">De lo contrario, contiene un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7cf5c-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf5c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7cf5c-114">Return value</span></span>

<span data-ttu-id="7cf5c-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7cf5c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7cf5c-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7cf5c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cf5c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cf5c-117">Requirements</span></span>



| <span data-ttu-id="7cf5c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cf5c-118">Requirement</span></span> | <span data-ttu-id="7cf5c-119">Value</span><span class="sxs-lookup"><span data-stu-id="7cf5c-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="7cf5c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cf5c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf5c-121">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="7cf5c-121">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="7cf5c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cf5c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf5c-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7cf5c-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7cf5c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cf5c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf5c-125">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="7cf5c-125">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





