---
title: Método IRDVTaskPluginNotifySink (Sbtsv. h)
description: El agente de tareas lo llama para solicitar que se cierre el agente de tareas.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Método de terminación Servicios de Escritorio remoto
- Método de finalización Servicios de Escritorio remoto, interfaz IRDVTaskPluginNotifySink
- Interfaz IRDVTaskPluginNotifySink Servicios de Escritorio remoto, método he terminado
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535320"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a><span data-ttu-id="32623-106">IRDVTaskPluginNotifySink:: alterminad (método)</span><span class="sxs-lookup"><span data-stu-id="32623-106">IRDVTaskPluginNotifySink::OnTerminated method</span></span>

<span data-ttu-id="32623-107">El agente de tareas lo llama para solicitar que se cierre el agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="32623-107">Called by the task agent to request that the task agent be shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="32623-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32623-108">Syntax</span></span>


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="32623-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32623-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32623-110">*HR* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32623-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32623-111">Indica si el apagado se debe a un apagado normal o a un error.</span><span class="sxs-lookup"><span data-stu-id="32623-111">Indicates if the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="32623-112">Si el apagado es normal, contiene **S \_ correctos**.</span><span class="sxs-lookup"><span data-stu-id="32623-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="32623-113">De lo contrario, contiene un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32623-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32623-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32623-114">Return value</span></span>

<span data-ttu-id="32623-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="32623-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="32623-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32623-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="32623-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32623-117">Requirements</span></span>



| <span data-ttu-id="32623-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="32623-118">Requirement</span></span> | <span data-ttu-id="32623-119">Value</span><span class="sxs-lookup"><span data-stu-id="32623-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32623-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32623-120">Minimum supported client</span></span><br/> | <span data-ttu-id="32623-121">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="32623-121">Windows 7 Enterprise</span></span><br/>                                                    |
| <span data-ttu-id="32623-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32623-122">Minimum supported server</span></span><br/> | <span data-ttu-id="32623-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32623-123">Windows Server 2008 R2</span></span><br/>                                                  |
| <span data-ttu-id="32623-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32623-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="32623-125"><dt>Sbtsv. h</dt></span><span class="sxs-lookup"><span data-stu-id="32623-125"><dt>Sbtsv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32623-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="32623-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32623-127">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="32623-127">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





