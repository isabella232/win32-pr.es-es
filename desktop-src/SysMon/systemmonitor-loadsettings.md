---
title: SystemMonitor. LoadSettings, método
description: Agrega los contadores del archivo de plantilla HTML al monitor de sistema.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Método LoadSettings SysMon
- Método LoadSettings SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Método LoadSettings
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422338"
---
# <a name="systemmonitorloadsettings-method"></a><span data-ttu-id="ad006-106">SystemMonitor. LoadSettings, método</span><span class="sxs-lookup"><span data-stu-id="ad006-106">SystemMonitor.LoadSettings method</span></span>

<span data-ttu-id="ad006-107">Agrega los contadores del archivo de plantilla HTML al monitor de sistema.</span><span class="sxs-lookup"><span data-stu-id="ad006-107">Adds the counters in the HTML template file to the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad006-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad006-108">Syntax</span></span>


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a><span data-ttu-id="ad006-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad006-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad006-110">*SettingsFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ad006-110">*SettingsFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad006-111">Cadena HTML que especifica los contadores que se van a agregar al monitor del sistema.</span><span class="sxs-lookup"><span data-stu-id="ad006-111">HTML string that specifies the counters to add to the System Monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad006-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad006-112">Return value</span></span>

<span data-ttu-id="ad006-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ad006-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad006-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad006-114">Remarks</span></span>

<span data-ttu-id="ad006-115">Para guardar los contadores actuales en el monitor de sistema en un archivo HTML, llame al método [**SystemMonitor. SaveAs**](systemmonitor-saveas.md) .</span><span class="sxs-lookup"><span data-stu-id="ad006-115">To save the current counters in the System Monitor to an HTML file, call the [**SystemMonitor.SaveAs**](systemmonitor-saveas.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad006-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad006-116">Requirements</span></span>



| <span data-ttu-id="ad006-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad006-117">Requirement</span></span> | <span data-ttu-id="ad006-118">Value</span><span class="sxs-lookup"><span data-stu-id="ad006-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad006-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad006-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ad006-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ad006-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad006-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad006-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ad006-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad006-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad006-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ad006-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad006-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ad006-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad006-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad006-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad006-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="ad006-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





