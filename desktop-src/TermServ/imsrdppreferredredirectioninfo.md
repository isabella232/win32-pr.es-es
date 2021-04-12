---
title: Interfaz IMsRdpPreferredRedirectionInfo
description: Proporciona una propiedad para controlar mediante un servidor de redirección.
ms.assetid: 1EAD9B15-4A84-4179-8A92-F0736B04B4F1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpPreferredRedirectionInfo
- Servicios de Escritorio remoto de la interfaz IMsRdpPreferredRedirectionInfo, descrito
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8ea28c36ca06548128954298e35c0cc20de5b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489509"
---
# <a name="imsrdppreferredredirectioninfo-interface"></a><span data-ttu-id="623a3-105">Interfaz IMsRdpPreferredRedirectionInfo</span><span class="sxs-lookup"><span data-stu-id="623a3-105">IMsRdpPreferredRedirectionInfo interface</span></span>

<span data-ttu-id="623a3-106">Proporciona una propiedad para controlar mediante un servidor de redirección.</span><span class="sxs-lookup"><span data-stu-id="623a3-106">Provides a property to control using a redirection server.</span></span>

## <a name="members"></a><span data-ttu-id="623a3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="623a3-107">Members</span></span>

<span data-ttu-id="623a3-108">La interfaz **IMsRdpPreferredRedirectionInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="623a3-108">The **IMsRdpPreferredRedirectionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="623a3-109">**IMsRdpPreferredRedirectionInfo** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="623a3-109">**IMsRdpPreferredRedirectionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="623a3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="623a3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="623a3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="623a3-111">Properties</span></span>

<span data-ttu-id="623a3-112">La interfaz **IMsRdpPreferredRedirectionInfo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="623a3-112">The **IMsRdpPreferredRedirectionInfo** interface has these properties.</span></span>



| <span data-ttu-id="623a3-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="623a3-113">Property</span></span>                                                                                               | <span data-ttu-id="623a3-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="623a3-114">Access type</span></span>           | <span data-ttu-id="623a3-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="623a3-115">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="623a3-116">**UseRedirectionServerName**</span><span class="sxs-lookup"><span data-stu-id="623a3-116">**UseRedirectionServerName**</span></span>](imsrdppreferredredirectioninfo-useredirectionservername.md)<br/> | <span data-ttu-id="623a3-117">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="623a3-117">Read/write</span></span><br/> | <span data-ttu-id="623a3-118">Obtiene y establece si se utiliza el nombre del servidor de redirección.</span><span class="sxs-lookup"><span data-stu-id="623a3-118">Gets and sets whether to use the redirection server name.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="623a3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="623a3-119">Requirements</span></span>



| <span data-ttu-id="623a3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="623a3-120">Requirement</span></span> | <span data-ttu-id="623a3-121">Value</span><span class="sxs-lookup"><span data-stu-id="623a3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="623a3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="623a3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="623a3-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="623a3-123">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="623a3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="623a3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="623a3-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="623a3-125">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="623a3-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="623a3-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="623a3-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="623a3-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="623a3-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="623a3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="623a3-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="623a3-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="623a3-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="623a3-130">CLSID</span></span><br/>                    | <span data-ttu-id="623a3-131">CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span><span class="sxs-lookup"><span data-stu-id="623a3-131">CLSID\_MsRdpClient10 is defined as C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span></span><br/> <span data-ttu-id="623a3-132">CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D</span><span class="sxs-lookup"><span data-stu-id="623a3-132">CLSID\_MsRdpClient10NotSafeForScripting is defined as A0C63C30-F08D-4AB4-907C-34905D770C7D</span></span><br/> <span data-ttu-id="623a3-133">CLSID \_ MsRdpClient7 se define como A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="623a3-133">CLSID\_MsRdpClient7 is defined as A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span><br/> <span data-ttu-id="623a3-134">CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="623a3-134">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span><br/> <span data-ttu-id="623a3-135">CLSID \_ MsRdpClient8 se define como 5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="623a3-135">CLSID\_MsRdpClient8 is defined as 5F681803-2900-4C43-A1CC-CF405404A676</span></span><br/> <span data-ttu-id="623a3-136">CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="623a3-136">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="623a3-137">CLSID \_ MsRdpClient9 se define como 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="623a3-137">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="623a3-138">CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="623a3-138">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="623a3-139">IID</span><span class="sxs-lookup"><span data-stu-id="623a3-139">IID</span></span><br/>                      | <span data-ttu-id="623a3-140">IID \_ IMsRdpPreferredRedirectionInfo se define como FDD029F9-9574-4DEF-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="623a3-140">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

