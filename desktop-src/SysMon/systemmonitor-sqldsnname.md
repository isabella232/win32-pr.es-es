---
title: Propiedad SqlDsnName de SystemMonitor
description: Recupera o establece el nombre del origen de datos ODBC (DSN).
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Propiedad SqlDsnName SysMon
- Propiedad SqlDsnName SysMon, interfaz SystemMonitor
- Interfaz SystemMonitor SysMon, propiedad SqlDsnName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421897"
---
# <a name="systemmonitorsqldsnname-property"></a><span data-ttu-id="623e7-106">SystemMonitor:: SqlDsnName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="623e7-106">SystemMonitor::SqlDsnName property</span></span>

<span data-ttu-id="623e7-107">Recupera o establece el nombre del origen de datos ODBC (DSN).</span><span class="sxs-lookup"><span data-stu-id="623e7-107">Retrieves or sets the ODBC data source name (DSN).</span></span>

## <a name="syntax"></a><span data-ttu-id="623e7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="623e7-108">Syntax</span></span>


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a><span data-ttu-id="623e7-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="623e7-109">Property value</span></span>

<span data-ttu-id="623e7-110">Nombre del origen de datos ODBC que apunta a una base de datos que contiene las tablas correctas de Perfmon.</span><span class="sxs-lookup"><span data-stu-id="623e7-110">ODBC data source name that points to a database that contains the correct Perfmon tables.</span></span> <span data-ttu-id="623e7-111">El formato es SQL: DSN.</span><span class="sxs-lookup"><span data-stu-id="623e7-111">The format is SQL:DSN.</span></span>

## <a name="remarks"></a><span data-ttu-id="623e7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="623e7-112">Remarks</span></span>

<span data-ttu-id="623e7-113">Debe usar el complemento de MMC Perfmon. msc para generar el archivo de registro de SQL.</span><span class="sxs-lookup"><span data-stu-id="623e7-113">You must use the Perfmon.msc MMC snap-in to generate the SQL log file.</span></span> <span data-ttu-id="623e7-114">Los registros de contador se encuentran en **registros y alertas de rendimiento**.</span><span class="sxs-lookup"><span data-stu-id="623e7-114">The counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="623e7-115">Para especificar un registro de SQL, haga clic con el botón secundario en el archivo de registro que creó y seleccione **propiedades** en el menú.</span><span class="sxs-lookup"><span data-stu-id="623e7-115">To specify an SQL log, right-click the log file you created and select **Properties** from the menu.</span></span> <span data-ttu-id="623e7-116">En la página de propiedades **archivos de registro** , seleccione **SQL Database** en el cuadro de lista desplegable tipo de **archivo de registro** .</span><span class="sxs-lookup"><span data-stu-id="623e7-116">On the **Log Files** property page, select **SQL Database** from the **Log file type** drop-down list box.</span></span>

<span data-ttu-id="623e7-117">**Antes de Windows Vista:** No se puede modificar esta propiedad si el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) está establecido en [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="623e7-117">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="623e7-118">En primer lugar, debe especificar el nombre y, a continuación, establecer **SystemMonitor. DataSourceType** en **DataSourceTypeConstants.sysmonSqlLog**.</span><span class="sxs-lookup"><span data-stu-id="623e7-118">You must first specify the name and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonSqlLog**.</span></span>

## <a name="requirements"></a><span data-ttu-id="623e7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="623e7-119">Requirements</span></span>



| <span data-ttu-id="623e7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="623e7-120">Requirement</span></span> | <span data-ttu-id="623e7-121">Value</span><span class="sxs-lookup"><span data-stu-id="623e7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="623e7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="623e7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="623e7-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="623e7-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="623e7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="623e7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="623e7-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="623e7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="623e7-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="623e7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="623e7-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="623e7-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="623e7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="623e7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="623e7-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="623e7-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="623e7-130">**SystemMonitor.SqlLogSetName**</span><span class="sxs-lookup"><span data-stu-id="623e7-130">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





