---
title: Interfaz ITSRemoteProgram
description: Incluye métodos para establecer y recuperar el modo RemoteApp y los parámetros de inicio para un programa RemoteApp, como la ruta de acceso del archivo ejecutable y el directorio de trabajo.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz ITSRemoteProgram
- Servicios de Escritorio remoto de la interfaz ITSRemoteProgram, descrito
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079513"
---
# <a name="itsremoteprogram-interface"></a><span data-ttu-id="959ad-105">Interfaz ITSRemoteProgram</span><span class="sxs-lookup"><span data-stu-id="959ad-105">ITSRemoteProgram interface</span></span>

<span data-ttu-id="959ad-106">Incluye métodos para establecer y recuperar el modo RemoteApp y los parámetros de inicio para un programa RemoteApp, como la ruta de acceso del archivo ejecutable y el directorio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="959ad-106">Includes methods to set and retrieve the RemoteApp mode and the start-up parameters for a RemoteApp program, such as the path of the executable file and the working directory.</span></span>

## <a name="members"></a><span data-ttu-id="959ad-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="959ad-107">Members</span></span>

<span data-ttu-id="959ad-108">La interfaz **ITSRemoteProgram** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="959ad-108">The **ITSRemoteProgram** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="959ad-109">**ITSRemoteProgram** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="959ad-109">**ITSRemoteProgram** also has these types of members:</span></span>

-   [<span data-ttu-id="959ad-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="959ad-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="959ad-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="959ad-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="959ad-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="959ad-112">Methods</span></span>

<span data-ttu-id="959ad-113">La interfaz **ITSRemoteProgram** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="959ad-113">The **ITSRemoteProgram** interface has these methods.</span></span>



| <span data-ttu-id="959ad-114">Método</span><span class="sxs-lookup"><span data-stu-id="959ad-114">Method</span></span>                                                            | <span data-ttu-id="959ad-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="959ad-115">Description</span></span>                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="959ad-116">**ServerStartProgram**</span><span class="sxs-lookup"><span data-stu-id="959ad-116">**ServerStartProgram**</span></span>](itsremoteprogram-serverstartprogram.md) | <span data-ttu-id="959ad-117">Especifica un programa RemoteApp para iniciarse en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="959ad-117">Specifies a RemoteApp program to start in the remote session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="959ad-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="959ad-118">Properties</span></span>

<span data-ttu-id="959ad-119">La interfaz **ITSRemoteProgram** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="959ad-119">The **ITSRemoteProgram** interface has these properties.</span></span>



| <span data-ttu-id="959ad-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="959ad-120">Property</span></span>                                                                   | <span data-ttu-id="959ad-121">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="959ad-121">Access type</span></span>           | <span data-ttu-id="959ad-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="959ad-122">Description</span></span>                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [<span data-ttu-id="959ad-123">**RemoteProgramMode**</span><span class="sxs-lookup"><span data-stu-id="959ad-123">**RemoteProgramMode**</span></span>](itsremoteprogram-remoteprogrammode.md)<br/> | <span data-ttu-id="959ad-124">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="959ad-124">Read/write</span></span><br/> | <span data-ttu-id="959ad-125">Modo RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="959ad-125">The RemoteApp mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="959ad-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="959ad-126">Requirements</span></span>



| <span data-ttu-id="959ad-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="959ad-127">Requirement</span></span> | <span data-ttu-id="959ad-128">Value</span><span class="sxs-lookup"><span data-stu-id="959ad-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="959ad-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="959ad-129">Minimum supported client</span></span><br/> | <span data-ttu-id="959ad-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="959ad-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="959ad-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="959ad-131">Minimum supported server</span></span><br/> | <span data-ttu-id="959ad-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="959ad-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="959ad-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="959ad-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="959ad-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="959ad-134"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="959ad-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="959ad-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="959ad-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="959ad-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="959ad-137">IID</span><span class="sxs-lookup"><span data-stu-id="959ad-137">IID</span></span><br/>                      | <span data-ttu-id="959ad-138">IID \_ ITSRemoteProgram se define como FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="959ad-138">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="959ad-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="959ad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="959ad-140">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="959ad-140">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="959ad-141">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="959ad-141">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

