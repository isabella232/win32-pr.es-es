---
description: Abre un cuadro de diálogo de sistema para solicitar permiso de usuario para dispositivos habilitados para la ubicación.
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: LocationDisp. LatLongReportFactory. RequestPermissions, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed789aca4b6c9d0db50a3e7b6cae33d55d22920c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678035"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a><span data-ttu-id="88a09-103">LocationDisp. LatLongReportFactory. RequestPermissions, método</span><span class="sxs-lookup"><span data-stu-id="88a09-103">LocationDisp.LatLongReportFactory.RequestPermissions method</span></span>

<span data-ttu-id="88a09-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="88a09-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="88a09-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="88a09-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="88a09-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88a09-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="88a09-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="88a09-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="88a09-108">Abre un cuadro de diálogo de sistema para solicitar permiso de usuario para dispositivos habilitados para la ubicación.</span><span class="sxs-lookup"><span data-stu-id="88a09-108">Opens a system dialog box to request user permission for location-enabled devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="88a09-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88a09-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a><span data-ttu-id="88a09-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88a09-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88a09-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="88a09-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="88a09-112">Este parámetro no se utiliza y debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="88a09-112">This parameter is not used and should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88a09-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88a09-113">Return value</span></span>

<span data-ttu-id="88a09-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="88a09-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88a09-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88a09-115">Remarks</span></span>

<span data-ttu-id="88a09-116">La llamada es sincrónica y el autor de la llamada espera a que se cierre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="88a09-116">The call is synchronous and the caller waits for the dialog box to be closed.</span></span>

> [!Note]  
> <span data-ttu-id="88a09-117">Si una aplicación que se ejecuta en modo protegido, como un objeto auxiliar de explorador (BHO) de Internet Explorer, llama a **RequestPermissions** y el usuario elige la opción **no habilitar este sensor de ubicación** en el cuadro de diálogo, el proveedor de ubicación no se habilitará, pero Windows volverá a mostrar el cuadro de diálogo si el mismo usuario llama a **RequestPermissions** de nuevo.</span><span class="sxs-lookup"><span data-stu-id="88a09-117">If an application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls **RequestPermissions**, and the user chooses the **Don't enable this location sensor** option in the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if **RequestPermissions** is called again by the same user.</span></span> <span data-ttu-id="88a09-118">Las aplicaciones que se ejecutan en modo protegido pueden optar por no llamar a **RequestPermissions** en el inicio para que el usuario no vea un cuadro de diálogo posiblemente no deseado cada vez que se inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88a09-118">Applications that run in protected mode may choose to not call **RequestPermissions** on startup so that the user does not see a possibly unwanted dialog box each time the application starts.</span></span>

 

## <a name="examples"></a><span data-ttu-id="88a09-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="88a09-119">Examples</span></span>

<span data-ttu-id="88a09-120">Para obtener un ejemplo de cómo usar este método, consulte [escucha de eventos de informe de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="88a09-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="88a09-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88a09-121">Requirements</span></span>



| <span data-ttu-id="88a09-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="88a09-122">Requirement</span></span> | <span data-ttu-id="88a09-123">Value</span><span class="sxs-lookup"><span data-stu-id="88a09-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="88a09-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88a09-124">Minimum supported client</span></span><br/> | <span data-ttu-id="88a09-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="88a09-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="88a09-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88a09-126">Minimum supported server</span></span><br/> | <span data-ttu-id="88a09-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="88a09-127">None supported</span></span><br/>                  |



 

