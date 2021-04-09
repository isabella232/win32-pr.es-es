---
title: Archivos de código para el ejemplo de proveedor de origen
description: Archivos de código para el ejemplo de proveedor de origen
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Administrador de dispositivos de Windows Media, ejemplos
- Administrador de dispositivos, ejemplos
- Windows Media Administrador de dispositivos, ejemplo de proveedor de servicios
- Administrador de dispositivos, ejemplo de proveedor de servicios
- proveedores de servicios, ejemplos
- ejemplos, proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148815"
---
# <a name="code-files-for-the-source-provider-sample"></a><span data-ttu-id="a1def-109">Archivos de código para el ejemplo de proveedor de origen</span><span class="sxs-lookup"><span data-stu-id="a1def-109">Code Files for the Source Provider Sample</span></span>

<span data-ttu-id="a1def-110">El proyecto de proveedor de origen de ejemplo incluye los siguientes archivos de código fuente, con encabezados asociados:</span><span class="sxs-lookup"><span data-stu-id="a1def-110">The sample source provider project includes the following source code files, with associated headers:</span></span>



| <span data-ttu-id="a1def-111">Archivo</span><span class="sxs-lookup"><span data-stu-id="a1def-111">File</span></span>                   | <span data-ttu-id="a1def-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1def-112">Description</span></span>                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1def-113">hdsppch. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-113">hdsppch.cpp</span></span>            | <span data-ttu-id="a1def-114">Incluye archivos ATL estándar.</span><span class="sxs-lookup"><span data-stu-id="a1def-114">Includes standard ATL files.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="a1def-115">clave. c</span><span class="sxs-lookup"><span data-stu-id="a1def-115">key.c</span></span>                  | <span data-ttu-id="a1def-116">Contiene una clave de autenticación ficticia.</span><span class="sxs-lookup"><span data-stu-id="a1def-116">Contains a dummy authentication key.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="a1def-117">loghelp. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-117">loghelp.cpp</span></span>            | <span data-ttu-id="a1def-118">Contiene funciones que registran la actividad y los errores mediante la clase **WMDMLogger** , que se implementa en el archivo de sistema WMDMLOG.dll.</span><span class="sxs-lookup"><span data-stu-id="a1def-118">Contains functions that log activity and errors by using the **WMDMLogger** class, which is implemented in the WMDMLOG.dll system file.</span></span>                                                                         |
| <span data-ttu-id="a1def-119">MDServiceProvider. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-119">MDServiceProvider.cpp</span></span>  | <span data-ttu-id="a1def-120">Implementa una clase, CMDServiceProvider, que implementa las interfaces [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) y IComponentAuthenticate.</span><span class="sxs-lookup"><span data-stu-id="a1def-120">Implements a class, CMDServiceProvider, that implements the [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) and IComponentAuthenticate interfaces.</span></span>                                                             |
| <span data-ttu-id="a1def-121">mdsp. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-121">mdsp.cpp</span></span>               | <span data-ttu-id="a1def-122">Código de registro y punto de entrada de DLL.</span><span class="sxs-lookup"><span data-stu-id="a1def-122">DLL entry point and registration code.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="a1def-123">MDSPDevice. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-123">MDSPDevice.cpp</span></span>         | <span data-ttu-id="a1def-124">Implementa una clase, CMDSPDevice, que implementa las interfaces [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)y **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="a1def-124">Implements a class, CMDSPDevice, that implements the [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol), and **ISpecifyPropertyPages** interfaces.</span></span>                          |
| <span data-ttu-id="a1def-125">MDSPEnumDevice. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-125">MDSPEnumDevice.cpp</span></span>     | <span data-ttu-id="a1def-126">Implementa una clase, CMDSPEnumDevice, que implementa la interfaz [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) .</span><span class="sxs-lookup"><span data-stu-id="a1def-126">Implements a class, CMDSPEnumDevice, that implements the [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) interface.</span></span>                                                                                                  |
| <span data-ttu-id="a1def-127">MDSPEnumStorage. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-127">MDSPEnumStorage.cpp</span></span>    | <span data-ttu-id="a1def-128">Implementa una clase, CMDSPEnumStorage, que implementa la interfaz [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) .</span><span class="sxs-lookup"><span data-stu-id="a1def-128">Implements a class, CMDSPEnumStorage, that implements the [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) interface.</span></span>                                                                                               |
| <span data-ttu-id="a1def-129">MDSPStorage. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-129">MDSPStorage.cpp</span></span>        | <span data-ttu-id="a1def-130">Implementa una clase, CMDSPStorage, que implementa las interfaces [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)y [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) .</span><span class="sxs-lookup"><span data-stu-id="a1def-130">Implements a class, CMDSPStorage, that implements the [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo), and [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) interfaces.</span></span>                    |
| <span data-ttu-id="a1def-131">MDSPStorageGlobals. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-131">MDSPStorageGlobals.cpp</span></span> | <span data-ttu-id="a1def-132">Implementa una clase, CMDSPStorageGlobals, que implementa la interfaz [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) .</span><span class="sxs-lookup"><span data-stu-id="a1def-132">Implements a class, CMDSPStorageGlobals, that implements the [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) interface.</span></span>                                                                                      |
| <span data-ttu-id="a1def-133">MDSPutil. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-133">MDSPutil.cpp</span></span>           | <span data-ttu-id="a1def-134">Contiene varias funciones de utilidad para la administración de dispositivos y archivos.</span><span class="sxs-lookup"><span data-stu-id="a1def-134">Contains various utility functions for device and file management.</span></span>                                                                                                                                              |
| <span data-ttu-id="a1def-135">PropPage. cpp</span><span class="sxs-lookup"><span data-stu-id="a1def-135">proppage.cpp</span></span>           | <span data-ttu-id="a1def-136">Implementa una clase, CPropPage, que hereda las clases ATL **IPropertyPageImpl** (para implementar IPropertyPage) y **CDialogImpl**, que hereda la clase de ATL CDialogImpl (para administrar mensajes y ventanas).</span><span class="sxs-lookup"><span data-stu-id="a1def-136">Implements a class, CPropPage, that inherits the ATL classes **IPropertyPageImpl** (to implement IPropertyPage) and **CDialogImpl**, which inherits the ATL class CDialogImpl (to manage windows and messages).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a1def-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1def-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1def-138">**Proveedor de servicios de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="a1def-138">**Sample Service Provider**</span></span>](sample-service-provider.md)
</dt> </dl>

 

 




