---
title: SystemMonitor. SaveAs (método)
description: Guarda los valores del contador en la vista del gráfico en un archivo de registro.
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- Método SaveAs SysMon
- Método SaveAs SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método SaveAs
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665981"
---
# <a name="systemmonitorsaveas-method"></a><span data-ttu-id="b1755-106">SystemMonitor. SaveAs (método)</span><span class="sxs-lookup"><span data-stu-id="b1755-106">SystemMonitor.SaveAs method</span></span>

<span data-ttu-id="b1755-107">Guarda los valores del contador en la vista del gráfico en un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b1755-107">Saves the counter values in the graph view to a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1755-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1755-108">Syntax</span></span>


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a><span data-ttu-id="b1755-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1755-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1755-110">*nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1755-110">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1755-111">Ruta de acceso del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b1755-111">File path of the log file.</span></span> <span data-ttu-id="b1755-112">Puede especificar la ruta de acceso como una ruta de acceso absoluta, relativa o UNC.</span><span class="sxs-lookup"><span data-stu-id="b1755-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="b1755-113">La extensión de nombre de archivo de registro debe ser. TSV o. htm.</span><span class="sxs-lookup"><span data-stu-id="b1755-113">The log file name extension must be either .tsv or .htm.</span></span> <span data-ttu-id="b1755-114">Si no existe una carpeta en la ruta de acceso, SYSMON la creará.</span><span class="sxs-lookup"><span data-stu-id="b1755-114">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="b1755-115">Si el archivo existe, se sobrescribe el archivo.</span><span class="sxs-lookup"><span data-stu-id="b1755-115">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="b1755-116">SYSMON aplica las ACL predeterminadas del directorio principal.</span><span class="sxs-lookup"><span data-stu-id="b1755-116">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="b1755-117">*filetype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1755-117">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1755-118">Formato de los datos de contador guardados en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b1755-118">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="b1755-119">Puede especificar [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) o **SysmonFileType.sysmonFileTsv**.</span><span class="sxs-lookup"><span data-stu-id="b1755-119">You can specify either [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1755-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1755-120">Return value</span></span>

<span data-ttu-id="b1755-121">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b1755-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1755-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1755-122">Remarks</span></span>

<span data-ttu-id="b1755-123">Solo se guardan los datos del contador visibles en la vista del gráfico (para el número real de puntos de datos guardados, vea [**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md)).</span><span class="sxs-lookup"><span data-stu-id="b1755-123">Only the counter data visible in the graph view is saved (for the actual number of data points saved, see [**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1755-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1755-124">Requirements</span></span>



| <span data-ttu-id="b1755-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1755-125">Requirement</span></span> | <span data-ttu-id="b1755-126">Value</span><span class="sxs-lookup"><span data-stu-id="b1755-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1755-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1755-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b1755-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b1755-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1755-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1755-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b1755-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1755-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1755-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1755-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1755-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b1755-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1755-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1755-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1755-134">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="b1755-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="b1755-135">**SystemMonitor. relog**</span><span class="sxs-lookup"><span data-stu-id="b1755-135">**SystemMonitor.Relog**</span></span>](systemmonitor-relog.md)
</dt> </dl>

 

 





