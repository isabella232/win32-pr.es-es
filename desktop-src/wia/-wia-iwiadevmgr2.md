---
description: La interfaz IWiaDevMgr2 se usa para crear y administrar dispositivos de adquisición de imágenes y registrarse para recibir eventos de dispositivo.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: Interfaz IWiaDevMgr2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909865"
---
# <a name="iwiadevmgr2-interface"></a><span data-ttu-id="5e2f1-103">Interfaz IWiaDevMgr2</span><span class="sxs-lookup"><span data-stu-id="5e2f1-103">IWiaDevMgr2 interface</span></span>

<span data-ttu-id="5e2f1-104">La interfaz **IWiaDevMgr2** se usa para crear y administrar dispositivos de adquisición de imágenes y registrarse para recibir eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-104">The **IWiaDevMgr2** interface is used to create and manage image acquisition devices and to register to receive device events.</span></span>

## <a name="members"></a><span data-ttu-id="5e2f1-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e2f1-105">Members</span></span>

<span data-ttu-id="5e2f1-106">La interfaz **IWiaDevMgr2** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5e2f1-106">The **IWiaDevMgr2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5e2f1-107">**IWiaDevMgr2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5e2f1-107">**IWiaDevMgr2** also has these types of members:</span></span>

-   [<span data-ttu-id="5e2f1-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="5e2f1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5e2f1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5e2f1-109">Methods</span></span>

<span data-ttu-id="5e2f1-110">La interfaz **IWiaDevMgr2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-110">The **IWiaDevMgr2** interface has these methods.</span></span>



| <span data-ttu-id="5e2f1-111">Método</span><span class="sxs-lookup"><span data-stu-id="5e2f1-111">Method</span></span>                                                                                    | <span data-ttu-id="5e2f1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e2f1-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e2f1-113">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="5e2f1-113">**CreateDevice**</span></span>](-wia-iwiadevmgr2-createdevice.md)                                     | <span data-ttu-id="5e2f1-114">Crea un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para un dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-114">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="5e2f1-115">**EnumDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="5e2f1-115">**EnumDeviceInfo**</span></span>](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | <span data-ttu-id="5e2f1-116">Crea un enumerador de información de propiedad para cada dispositivo WIA 2,0 disponible.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-116">Creates an enumerator of property information for each available WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="5e2f1-117">**GetImageDlg**</span><span class="sxs-lookup"><span data-stu-id="5e2f1-117">**GetImageDlg**</span></span>](-wia-iwiadevmgr2-getimagedlg.md)                                       | <span data-ttu-id="5e2f1-118">El método [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) muestra uno o varios cuadros de diálogo que permiten a un usuario adquirir una imagen de un dispositivo WIA 2,0 y escribir la imagen en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-118">The [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method displays one or more dialog boxes that enable a user to acquire an image from a WIA 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="5e2f1-119">Este método extiende la funcionalidad de [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular la adquisición de imágenes en una única llamada API.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-119">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span> <br/> |
| [<span data-ttu-id="5e2f1-120">**RegisterEventCallbackCLSID**</span><span class="sxs-lookup"><span data-stu-id="5e2f1-120">**RegisterEventCallbackCLSID**</span></span>](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | <span data-ttu-id="5e2f1-121">El método [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) registra una aplicación para recibir eventos incluso si la aplicación no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-121">The [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) method registers an application to receive events even if the application is not running.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="5e2f1-122">**RegisterEventCallbackInterface**</span><span class="sxs-lookup"><span data-stu-id="5e2f1-122">**RegisterEventCallbackInterface**</span></span>](-wia-iwiadevmgr2-registereventcallbackinterface.md) | <span data-ttu-id="5e2f1-123">Registra una aplicación en ejecución para la notificación de eventos de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-123">Registers a running application for WIA 2.0 event notification.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="5e2f1-124">**RegisterEventCallbackProgram**</span><span class="sxs-lookup"><span data-stu-id="5e2f1-124">**RegisterEventCallbackProgram**</span></span>](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | <span data-ttu-id="5e2f1-125">El método [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) registra una aplicación para recibir eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-125">The [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method registers an application to receive device events.</span></span> <span data-ttu-id="5e2f1-126">Se proporciona principalmente para la compatibilidad con versiones anteriores de aplicaciones que no se escribieron para WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-126">It is primarily provided for backward compatibility with applications that were not written for WIA 2.0.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="5e2f1-127">**SelectDeviceDlg**</span><span class="sxs-lookup"><span data-stu-id="5e2f1-127">**SelectDeviceDlg**</span></span>](-wia-iwiadevmgr2-selectdevicedlg.md)                               | <span data-ttu-id="5e2f1-128">Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-128">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="5e2f1-129">**SelectDeviceDlgID**</span><span class="sxs-lookup"><span data-stu-id="5e2f1-129">**SelectDeviceDlgID**</span></span>](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | <span data-ttu-id="5e2f1-130">Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-130">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="5e2f1-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e2f1-131">Remarks</span></span>

<span data-ttu-id="5e2f1-132">La interfaz **IWiaDevMgr2** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5e2f1-132">The **IWiaDevMgr2** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="5e2f1-133">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e2f1-133">IUnknown Methods</span></span>                                        | <span data-ttu-id="5e2f1-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e2f1-134">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="5e2f1-135">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="5e2f1-135">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="5e2f1-136">Devuelve punteros a las interfaces compatibles.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-136">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="5e2f1-137">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="5e2f1-137">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="5e2f1-138">Incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-138">Increments reference count.</span></span>               |
| [<span data-ttu-id="5e2f1-139">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="5e2f1-139">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="5e2f1-140">Reduce el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="5e2f1-140">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="5e2f1-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e2f1-141">Requirements</span></span>



| <span data-ttu-id="5e2f1-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e2f1-142">Requirement</span></span> | <span data-ttu-id="5e2f1-143">Value</span><span class="sxs-lookup"><span data-stu-id="5e2f1-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2f1-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e2f1-144">Minimum supported client</span></span><br/> | <span data-ttu-id="5e2f1-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e2f1-145">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e2f1-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e2f1-146">Minimum supported server</span></span><br/> | <span data-ttu-id="5e2f1-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e2f1-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e2f1-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e2f1-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e2f1-149"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e2f1-149"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e2f1-150">IDL</span><span class="sxs-lookup"><span data-stu-id="5e2f1-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e2f1-151"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e2f1-151"><dt>Wia.idl</dt></span></span> </dl> |



 

 
