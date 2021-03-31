---
title: Propiedad DataSourceType SystemMonitor
description: Recupera o establece el origen de los datos del contador de rendimiento.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Propiedad DataSourceType SysMon
- Propiedad DataSourceType SysMon, interfaz SystemMonitor
- Interfaz SystemMonitor SysMon, propiedad DataSourceType
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079587"
---
# <a name="systemmonitordatasourcetype-property"></a><span data-ttu-id="1d7e8-106">SystemMonitor::D propiedad ataSourceType</span><span class="sxs-lookup"><span data-stu-id="1d7e8-106">SystemMonitor::DataSourceType property</span></span>

<span data-ttu-id="1d7e8-107">Recupera o establece el origen de los datos del contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-107">Retrieves or sets the source of the performance counter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d7e8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d7e8-108">Syntax</span></span>


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="1d7e8-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1d7e8-109">Property value</span></span>

<span data-ttu-id="1d7e8-110">Origen de los datos del contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-110">Source of the performance counter data.</span></span> <span data-ttu-id="1d7e8-111">Para obtener los valores posibles, vea [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="1d7e8-111">For possible values, see [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="1d7e8-112">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1d7e8-112">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d7e8-113">Tipo de excepción</span><span class="sxs-lookup"><span data-stu-id="1d7e8-113">Exception type</span></span></th>
<th><span data-ttu-id="1d7e8-114">Condición</span><span class="sxs-lookup"><span data-stu-id="1d7e8-114">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1d7e8-115"><strong>System.ArgumentException</strong></span><span class="sxs-lookup"><span data-stu-id="1d7e8-115"><strong>System.ArgumentException</strong></span></span></td>
<td><span data-ttu-id="1d7e8-116">Puede recibir esta excepción por una de las siguientes razones:</span><span class="sxs-lookup"><span data-stu-id="1d7e8-116">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="1d7e8-117">El valor de origen de datos especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-117">The specified data source value is not valid.</span></span></li>
<li><span data-ttu-id="1d7e8-118">Si el origen de datos es un archivo de registro, SYSMON no puede encontrar uno de los archivos especificados.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-118">If the data source is a log file, SYSMON cannot find one of the specified files.</span></span> <span data-ttu-id="1d7e8-119">El valor de Err. number es 0xC0000BD1.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-119">The Err.Number value is 0xC0000BD1.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1d7e8-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d7e8-120">Remarks</span></span>

<span data-ttu-id="1d7e8-121">**Antes de Windows Vista:** No puede Agregar o quitar archivos de registro de la [**colección de archivos de registro**](systemmonitor-logfiles.md) si el valor de esta propiedad se establece en sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-121">**Prior to Windows Vista:** You cannot add or remove a log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of this property is set to sysmonLogFiles.</span></span> <span data-ttu-id="1d7e8-122">Establezca el valor de esta propiedad en sysmonLogFiles después de crear o modificar la colección de archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-122">Only set the value of this property to sysmonLogFiles after creating or modifying the log file collection.</span></span>

<span data-ttu-id="1d7e8-123">Además, no se pueden modificar las propiedades [**SqlDsnName**](systemmonitor-sqldsnname.md) y [**SqlLogSetName**](systemmonitor-sqllogsetname.md) si el valor de esta propiedad no se debe establecer en sysmonSqlLog.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-123">Also, you cannot modify the [**SqlDsnName**](systemmonitor-sqldsnname.md) and [**SqlLogSetName**](systemmonitor-sqllogsetname.md) properties if the value of this property must not be set to sysmonSqlLog.</span></span> <span data-ttu-id="1d7e8-124">Establezca el valor de esta propiedad en sysmonSqlLog después de modificar los nombres del servidor y de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1d7e8-124">Only set the value of this property to sysmonSqlLog after modifying the server and database names.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d7e8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d7e8-125">Requirements</span></span>



| <span data-ttu-id="1d7e8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d7e8-126">Requirement</span></span> | <span data-ttu-id="1d7e8-127">Value</span><span class="sxs-lookup"><span data-stu-id="1d7e8-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d7e8-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d7e8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1d7e8-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1d7e8-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1d7e8-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d7e8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1d7e8-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d7e8-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d7e8-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d7e8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d7e8-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1d7e8-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d7e8-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d7e8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d7e8-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="1d7e8-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





