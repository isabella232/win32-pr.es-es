---
title: Interfaz IWMDRMDeviceApp2
description: La interfaz IWMDRMDeviceApp2 extiende IWMDRMDeviceApp proporcionando una nueva versión del método QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interfaz IWMDRMDeviceApp2 Administrador de dispositivos de Windows Media
- Interfaz IWMDRMDeviceApp2 de Windows Media Administrador de dispositivos, se describe
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358305"
---
# <a name="iwmdrmdeviceapp2-interface"></a><span data-ttu-id="14011-105">Interfaz IWMDRMDeviceApp2</span><span class="sxs-lookup"><span data-stu-id="14011-105">IWMDRMDeviceApp2 interface</span></span>

<span data-ttu-id="14011-106">La interfaz **IWMDRMDeviceApp2** extiende [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) proporcionando una nueva versión del método [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="14011-106">The **IWMDRMDeviceApp2** interface extends [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) by providing a new version of the [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) method.</span></span> <span data-ttu-id="14011-107">**QueryDeviceStatus2** permite al autor de la llamada consultar un requisito específico de DRM.</span><span class="sxs-lookup"><span data-stu-id="14011-107">**QueryDeviceStatus2** enables the caller to query for a specific DRM requirement.</span></span>

<span data-ttu-id="14011-108">Para obtener esta interfaz, llame a **CoCreateInstance** y pase CLSID \_ WMDRMDeviceApp.</span><span class="sxs-lookup"><span data-stu-id="14011-108">To get this interface, call **CoCreateInstance** and pass in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="14011-109">Esta interfaz se define en el archivo de encabezado generado a partir de WMDRMDeviceApp. idl.</span><span class="sxs-lookup"><span data-stu-id="14011-109">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="14011-110">Este encabezado **\# incluye** "WMDM. h".</span><span class="sxs-lookup"><span data-stu-id="14011-110">This header **\#includes** "wmdm.h".</span></span> <span data-ttu-id="14011-111">Es posible que deba cambiar este nombre de archivo para que coincida con el encabezado generado a partir de WMDM. idl.</span><span class="sxs-lookup"><span data-stu-id="14011-111">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="14011-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="14011-112">Members</span></span>

<span data-ttu-id="14011-113">La interfaz **IWMDRMDeviceApp2** hereda de [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span><span class="sxs-lookup"><span data-stu-id="14011-113">The **IWMDRMDeviceApp2** interface inherits from [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span></span> <span data-ttu-id="14011-114">**IWMDRMDeviceApp2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="14011-114">**IWMDRMDeviceApp2** also has these types of members:</span></span>

-   [<span data-ttu-id="14011-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="14011-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="14011-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="14011-116">Methods</span></span>

<span data-ttu-id="14011-117">La interfaz **IWMDRMDeviceApp2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="14011-117">The **IWMDRMDeviceApp2** interface has these methods.</span></span>



| <span data-ttu-id="14011-118">Método</span><span class="sxs-lookup"><span data-stu-id="14011-118">Method</span></span>                                                            | <span data-ttu-id="14011-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="14011-119">Description</span></span>                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="14011-120">**QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="14011-120">**QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md) | <span data-ttu-id="14011-121">Consulta un dispositivo para una funcionalidad o estado DRM específico.</span><span class="sxs-lookup"><span data-stu-id="14011-121">Queries a device for a specific DRM status or capability.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="14011-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="14011-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14011-123">**IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="14011-123">**IWMDRMDeviceApp**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="14011-124">**Control del contenido protegido en la aplicación**</span><span class="sxs-lookup"><span data-stu-id="14011-124">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="14011-125">**Interfaces para aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="14011-125">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="14011-126">**Uso del contenido de disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="14011-126">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

 





