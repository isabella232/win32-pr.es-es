---
title: Propiedad SqlLogSetName de SystemMonitor
description: Recupera o establece el nombre descriptivo del conjunto de registros.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Propiedad SqlLogSetName SysMon
- Propiedad SqlLogSetName SysMon, interfaz SystemMonitor
- Interfaz SystemMonitor SysMon, propiedad SqlLogSetName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078827"
---
# <a name="systemmonitorsqllogsetname-property"></a><span data-ttu-id="52d3c-106">SystemMonitor:: SqlLogSetName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="52d3c-106">SystemMonitor::SqlLogSetName property</span></span>

<span data-ttu-id="52d3c-107">Recupera o establece el nombre descriptivo del conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="52d3c-107">Retrieves or sets the friendly name of the log set.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d3c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52d3c-108">Syntax</span></span>


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a><span data-ttu-id="52d3c-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="52d3c-109">Property value</span></span>

<span data-ttu-id="52d3c-110">Nombre descriptivo del conjunto de registros, que corresponde a un único archivo de registro que contiene datos binarios o de texto en la base de datos SQL.</span><span class="sxs-lookup"><span data-stu-id="52d3c-110">Friendly name of the log set, which corresponds to a single log file containing binary or text data in the SQL database.</span></span>

## <a name="remarks"></a><span data-ttu-id="52d3c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52d3c-111">Remarks</span></span>

<span data-ttu-id="52d3c-112">**Antes de Windows Vista:** No se puede modificar esta propiedad si el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) se establece en sysmonSqlLog.</span><span class="sxs-lookup"><span data-stu-id="52d3c-112">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonSqlLog.</span></span>

## <a name="requirements"></a><span data-ttu-id="52d3c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52d3c-113">Requirements</span></span>



| <span data-ttu-id="52d3c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52d3c-114">Requirement</span></span> | <span data-ttu-id="52d3c-115">Value</span><span class="sxs-lookup"><span data-stu-id="52d3c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52d3c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52d3c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52d3c-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="52d3c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="52d3c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52d3c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52d3c-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="52d3c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52d3c-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52d3c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52d3c-121"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="52d3c-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d3c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="52d3c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d3c-123">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="52d3c-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="52d3c-124">**SystemMonitor.SqlDsnName**</span><span class="sxs-lookup"><span data-stu-id="52d3c-124">**SystemMonitor.SqlDsnName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





