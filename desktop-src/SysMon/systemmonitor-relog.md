---
title: SystemMonitor. relog (método)
description: Vuelve a registrar los datos del contador en un nuevo archivo. También puede utilizar este método para especificar un nuevo tipo de archivo y para reducir el número de ejemplos que contiene el archivo de registro.
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- Relog (método) SysMon
- Método relog SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método relog
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150162"
---
# <a name="systemmonitorrelog-method"></a><span data-ttu-id="000d5-107">SystemMonitor. relog (método)</span><span class="sxs-lookup"><span data-stu-id="000d5-107">SystemMonitor.Relog method</span></span>

<span data-ttu-id="000d5-108">Vuelve a registrar los datos del contador en un nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="000d5-108">Relogs the counter data to a new file.</span></span> <span data-ttu-id="000d5-109">También puede utilizar este método para especificar un nuevo tipo de archivo y para reducir el número de ejemplos que contiene el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="000d5-109">You can also use this method to specify a new file type and to reduce the number of samples contained in the log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="000d5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="000d5-110">Syntax</span></span>


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="000d5-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="000d5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="000d5-112">*nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="000d5-112">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="000d5-113">Ruta de acceso del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="000d5-113">File path of the log file.</span></span> <span data-ttu-id="000d5-114">Puede especificar la ruta de acceso como una ruta de acceso absoluta, relativa o UNC.</span><span class="sxs-lookup"><span data-stu-id="000d5-114">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="000d5-115">La extensión de nombre de archivo de registro debe ser. BLG,. TSV o. csv.</span><span class="sxs-lookup"><span data-stu-id="000d5-115">The log file name extension must be either .blg, .tsv, or .csv.</span></span> <span data-ttu-id="000d5-116">Si no existe una carpeta en la ruta de acceso, SYSMON la creará.</span><span class="sxs-lookup"><span data-stu-id="000d5-116">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="000d5-117">Si el archivo existe, se sobrescribe el archivo.</span><span class="sxs-lookup"><span data-stu-id="000d5-117">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="000d5-118">SYSMON aplica las ACL predeterminadas del directorio principal.</span><span class="sxs-lookup"><span data-stu-id="000d5-118">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="000d5-119">*filetype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="000d5-119">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="000d5-120">Formato de los datos de contador guardados en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="000d5-120">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="000d5-121">Puede especificar [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysMonFileCsv** o **SysmonFileType.sysmonFileTsv**.</span><span class="sxs-lookup"><span data-stu-id="000d5-121">You can specify either [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonFileCsv**, or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> <dt>

<span data-ttu-id="000d5-122">*filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="000d5-122">*filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="000d5-123">Número de muestras de los archivos de registro antiguos que se van a guardar en el nuevo archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="000d5-123">Number of samples from the old log files to save in the new log file.</span></span> <span data-ttu-id="000d5-124">Especifique 1 para guardar todos los ejemplos de los archivos antiguos en los nuevos archivos.</span><span class="sxs-lookup"><span data-stu-id="000d5-124">Specify 1 to save every sample from the old files to the new files.</span></span> <span data-ttu-id="000d5-125">Especifique 2 para guardar una de cada dos muestras del archivo anterior.</span><span class="sxs-lookup"><span data-stu-id="000d5-125">Specify 2 to save one out of every two samples from the old file.</span></span> <span data-ttu-id="000d5-126">Especifique 3 para guardar una de cada tres muestras del archivo anterior.</span><span class="sxs-lookup"><span data-stu-id="000d5-126">Specify 3 to save one out of every three samples from the old file.</span></span> <span data-ttu-id="000d5-127">y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="000d5-127">And so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="000d5-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="000d5-128">Return value</span></span>

<span data-ttu-id="000d5-129">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="000d5-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="000d5-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="000d5-130">Remarks</span></span>

<span data-ttu-id="000d5-131">Este método usa los archivos de registro contenidos en la colección [**SystemMonitor. logfiles**](systemmonitor-logfiles.md) para reregistrar los datos del contador.</span><span class="sxs-lookup"><span data-stu-id="000d5-131">This method uses the log files contained in the [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md) collection to relog the counter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="000d5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="000d5-132">Requirements</span></span>



| <span data-ttu-id="000d5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="000d5-133">Requirement</span></span> | <span data-ttu-id="000d5-134">Value</span><span class="sxs-lookup"><span data-stu-id="000d5-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="000d5-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="000d5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="000d5-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="000d5-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="000d5-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="000d5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="000d5-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="000d5-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="000d5-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="000d5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="000d5-140"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="000d5-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="000d5-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="000d5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="000d5-142">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="000d5-142">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="000d5-143">**SystemMonitor. SaveAs**</span><span class="sxs-lookup"><span data-stu-id="000d5-143">**SystemMonitor.SaveAs**</span></span>](systemmonitor-saveas.md)
</dt> </dl>

 

 





