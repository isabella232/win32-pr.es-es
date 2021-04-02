---
description: Administra los informes de latitud y longitud.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: Objeto LocationDisp. LatLongReportFactory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913510"
---
# <a name="locationdisplatlongreportfactory-object"></a><span data-ttu-id="17e4f-103">Objeto LocationDisp. LatLongReportFactory</span><span class="sxs-lookup"><span data-stu-id="17e4f-103">LocationDisp.LatLongReportFactory object</span></span>

<span data-ttu-id="17e4f-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="17e4f-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="17e4f-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="17e4f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="17e4f-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17e4f-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="17e4f-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="17e4f-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="17e4f-108">Administra los informes de latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="17e4f-108">Manages latitude/longitude reports.</span></span>

## <a name="members"></a><span data-ttu-id="17e4f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="17e4f-109">Members</span></span>

<span data-ttu-id="17e4f-110">El objeto **LocationDisp. LatLongReportFactory** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="17e4f-110">The **LocationDisp.LatLongReportFactory** object has these types of members:</span></span>

-   [<span data-ttu-id="17e4f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="17e4f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="17e4f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17e4f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="17e4f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="17e4f-113">Methods</span></span>

<span data-ttu-id="17e4f-114">El objeto **LocationDisp. LatLongReportFactory** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="17e4f-114">The **LocationDisp.LatLongReportFactory** object has these methods.</span></span>



| <span data-ttu-id="17e4f-115">Método</span><span class="sxs-lookup"><span data-stu-id="17e4f-115">Method</span></span>                                                                                       | <span data-ttu-id="17e4f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="17e4f-116">Description</span></span>                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17e4f-117">**ListenForReports**</span><span class="sxs-lookup"><span data-stu-id="17e4f-117">**ListenForReports**</span></span>](locationdisp-latlongreportfactory-listenforreports.md)               | <span data-ttu-id="17e4f-118">Solicita eventos de informe de latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="17e4f-118">Requests latitude/longitude report events.</span></span><br/>                                         |
| [<span data-ttu-id="17e4f-119">**RequestPermissions**</span><span class="sxs-lookup"><span data-stu-id="17e4f-119">**RequestPermissions**</span></span>](locationdisp-latlongreportfactory-requestpermissions.md)           | <span data-ttu-id="17e4f-120">Abre un cuadro de diálogo de sistema para solicitar permiso de usuario para dispositivos habilitados para la ubicación.</span><span class="sxs-lookup"><span data-stu-id="17e4f-120">Opens a system dialog box to request user permission for location-enabled devices.</span></span><br/> |
| <span data-ttu-id="17e4f-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17e4f-121">[**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85))</span></span> | <span data-ttu-id="17e4f-122">Cancela las solicitudes de eventos de informe de latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="17e4f-122">Cancels requests for latitude/longitude report events.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="17e4f-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17e4f-123">Properties</span></span>

<span data-ttu-id="17e4f-124">El objeto **LocationDisp. LatLongReportFactory** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="17e4f-124">The **LocationDisp.LatLongReportFactory** object has these properties.</span></span>



| <span data-ttu-id="17e4f-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="17e4f-125">Property</span></span>                                                                                | <span data-ttu-id="17e4f-126">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="17e4f-126">Access type</span></span>           | <span data-ttu-id="17e4f-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="17e4f-127">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17e4f-128">**DesiredAccuracy**</span><span class="sxs-lookup"><span data-stu-id="17e4f-128">**DesiredAccuracy**</span></span>](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | <span data-ttu-id="17e4f-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="17e4f-129">Read/write</span></span><br/> | <span data-ttu-id="17e4f-130">Valor de precisión deseado actual.</span><span class="sxs-lookup"><span data-stu-id="17e4f-130">The current desired-accuracy value.</span></span><br/>                                                   |
| [<span data-ttu-id="17e4f-131">**LatLongReport**</span><span class="sxs-lookup"><span data-stu-id="17e4f-131">**LatLongReport**</span></span>](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | <span data-ttu-id="17e4f-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="17e4f-132">Read-only</span></span><br/>  | <span data-ttu-id="17e4f-133">Actual [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md).</span><span class="sxs-lookup"><span data-stu-id="17e4f-133">The current [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span><br/> |
| [<span data-ttu-id="17e4f-134">**ReportInterval**</span><span class="sxs-lookup"><span data-stu-id="17e4f-134">**ReportInterval**</span></span>](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | <span data-ttu-id="17e4f-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="17e4f-135">Read/write</span></span><br/> | <span data-ttu-id="17e4f-136">El intervalo de eventos de informe de latitud y longitud actual en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="17e4f-136">The current latitude/longitude report event interval in milliseconds.</span></span><br/>                 |
| [<span data-ttu-id="17e4f-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="17e4f-137">**Status**</span></span>](locationdisp-latlongreportfactory-status.md)<br/>                   | <span data-ttu-id="17e4f-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="17e4f-138">Read-only</span></span><br/>  | <span data-ttu-id="17e4f-139">Estado actual del informe.</span><span class="sxs-lookup"><span data-stu-id="17e4f-139">The current report status.</span></span><br/>                                                            |



 

## <a name="examples"></a><span data-ttu-id="17e4f-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="17e4f-140">Examples</span></span>

<span data-ttu-id="17e4f-141">En el código de ejemplo siguiente se muestra cómo crear este objeto en código HTML.</span><span class="sxs-lookup"><span data-stu-id="17e4f-141">The following example code shows how to create this object in HTML code.</span></span>


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



<span data-ttu-id="17e4f-142">En el ejemplo de código siguiente se muestra cómo crear este objeto en JScript con Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="17e4f-142">The following example code shows how to create this object in JScript using Windows Script Host.</span></span>


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



<span data-ttu-id="17e4f-143">En el ejemplo de código siguiente se muestra cómo crear este objeto en VBScript mediante Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="17e4f-143">The following example code shows how to create this object in VBScript using Windows Script Host.</span></span>


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a><span data-ttu-id="17e4f-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17e4f-144">Requirements</span></span>



| <span data-ttu-id="17e4f-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="17e4f-145">Requirement</span></span> | <span data-ttu-id="17e4f-146">Value</span><span class="sxs-lookup"><span data-stu-id="17e4f-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="17e4f-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17e4f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="17e4f-148">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="17e4f-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="17e4f-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17e4f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="17e4f-150">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="17e4f-150">None supported</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="17e4f-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="17e4f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e4f-152">**LocationDisp.DispLatLongReport**</span><span class="sxs-lookup"><span data-stu-id="17e4f-152">**LocationDisp.DispLatLongReport**</span></span>](locationdisp-displatlongreport.md)
</dt> </dl>

 

