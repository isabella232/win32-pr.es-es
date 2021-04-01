---
title: LogFiles. Add (método)
description: Agrega un archivo de registro a la colección.
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- Agregar método SysMon
- Agregar método SysMon, logfiles (clase)
- Logfiles (clase) SysMon, Add (método)
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150335"
---
# <a name="logfilesadd-method"></a><span data-ttu-id="907f8-106">LogFiles. Add (método)</span><span class="sxs-lookup"><span data-stu-id="907f8-106">LogFiles.Add method</span></span>

<span data-ttu-id="907f8-107">Agrega un archivo de registro a la colección.</span><span class="sxs-lookup"><span data-stu-id="907f8-107">Adds a log file to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="907f8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="907f8-108">Syntax</span></span>


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a><span data-ttu-id="907f8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="907f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="907f8-110">*nombreruta* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="907f8-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="907f8-111">Ruta de acceso al archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="907f8-111">Path to the log file.</span></span> <span data-ttu-id="907f8-112">Puede especificar la ruta de acceso como una ruta de acceso absoluta, relativa o UNC.</span><span class="sxs-lookup"><span data-stu-id="907f8-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="907f8-113">La extensión de nombre de archivo de registro debe ser. csv,. TSV o. BLG.</span><span class="sxs-lookup"><span data-stu-id="907f8-113">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="907f8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="907f8-114">Remarks</span></span>

<span data-ttu-id="907f8-115">Debe usar la herramienta Logman.exe o el complemento MMC Perfmon. msc para generar los archivos de registro que se agregan a esta colección.</span><span class="sxs-lookup"><span data-stu-id="907f8-115">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="907f8-116">En el caso de Perfmon. msc, los registros de contador se encuentran en **registros y alertas de rendimiento**.</span><span class="sxs-lookup"><span data-stu-id="907f8-116">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="907f8-117">Para obtener información detallada sobre el uso de Logman.exe o Perfmon. msc, busque Logman o use performance, respectivamente, en el **centro de ayuda y soporte técnico**.</span><span class="sxs-lookup"><span data-stu-id="907f8-117">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

<span data-ttu-id="907f8-118">**Antes de Windows Vista:** No puede Agregar archivos de registro a la [**colección de archivos de registro**](systemmonitor-logfiles.md) si el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) está establecido en [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="907f8-118">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="907f8-119">En primer lugar, establezca **SystemMonitor. DataSourceType** en **DataSourceTypeConstants.sysmonNullDataSource**, agregue los archivos de registro y los contadores y, a continuación, establezca **SystemMonitor. DataSourceType** en **DataSourceTypeConstants.sysmonLogFiles**.</span><span class="sxs-lookup"><span data-stu-id="907f8-119">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

## <a name="requirements"></a><span data-ttu-id="907f8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="907f8-120">Requirements</span></span>



| <span data-ttu-id="907f8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="907f8-121">Requirement</span></span> | <span data-ttu-id="907f8-122">Value</span><span class="sxs-lookup"><span data-stu-id="907f8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="907f8-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="907f8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="907f8-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="907f8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="907f8-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="907f8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="907f8-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="907f8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="907f8-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="907f8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="907f8-128"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="907f8-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="907f8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="907f8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="907f8-130">LogFiles</span><span class="sxs-lookup"><span data-stu-id="907f8-130">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="907f8-131">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="907f8-131">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="907f8-132">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="907f8-132">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





