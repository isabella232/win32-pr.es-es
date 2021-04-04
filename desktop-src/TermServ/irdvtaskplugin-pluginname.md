---
title: Propiedad IRDVTaskPlugin PluginName (Tspubplugincom. h)
description: Contiene el nombre para mostrar del agente de tareas.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PluginName
- Propiedad PluginName Servicios de Escritorio remoto, interfaz IRDVTaskPlugin
- Servicios de Escritorio remoto de la interfaz IRDVTaskPlugin, propiedad PluginName
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802707"
---
# <a name="irdvtaskpluginpluginname-property"></a><span data-ttu-id="de1ac-106">IRDVTaskPlugin::P propiedad luginName</span><span class="sxs-lookup"><span data-stu-id="de1ac-106">IRDVTaskPlugin::PluginName property</span></span>

<span data-ttu-id="de1ac-107">Contiene el nombre para mostrar del agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="de1ac-107">Contains the display name of the task agent.</span></span> <span data-ttu-id="de1ac-108">Este nombre se usa solo con fines de registro.</span><span class="sxs-lookup"><span data-stu-id="de1ac-108">This name is used for logging purposes only.</span></span>

<span data-ttu-id="de1ac-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="de1ac-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="de1ac-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de1ac-110">Syntax</span></span>


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="de1ac-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="de1ac-111">Property value</span></span>

<span data-ttu-id="de1ac-112">Nombre para mostrar del agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="de1ac-112">The display name of the task agent.</span></span>

## <a name="requirements"></a><span data-ttu-id="de1ac-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de1ac-113">Requirements</span></span>



| <span data-ttu-id="de1ac-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="de1ac-114">Requirement</span></span> | <span data-ttu-id="de1ac-115">Value</span><span class="sxs-lookup"><span data-stu-id="de1ac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="de1ac-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de1ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de1ac-117">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="de1ac-117">Windows 7 Enterprise</span></span><br/>                                                             |
| <span data-ttu-id="de1ac-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de1ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de1ac-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de1ac-119">Windows Server 2008 R2</span></span><br/>                                                           |
| <span data-ttu-id="de1ac-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de1ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de1ac-121"><dt>Tspubplugincom. h</dt></span><span class="sxs-lookup"><span data-stu-id="de1ac-121"><dt>Tspubplugincom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de1ac-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="de1ac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de1ac-123">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="de1ac-123">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





