---
description: El instalador establece la propiedad MsiNTProductType para los sistemas operativos Windows NT, Windows 2000 y versiones posteriores.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Propiedad MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671202"
---
# <a name="msintproducttype-property"></a><span data-ttu-id="79b97-103">Propiedad MsiNTProductType</span><span class="sxs-lookup"><span data-stu-id="79b97-103">MsiNTProductType property</span></span>

<span data-ttu-id="79b97-104">El instalador establece la propiedad **MsiNTProductType** para los sistemas operativos Windows NT, Windows 2000 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="79b97-104">The installer sets the **MsiNTProductType** property for Windows NT, Windows 2000, and later operating systems.</span></span> <span data-ttu-id="79b97-105">Esta propiedad indica el tipo de producto de Windows.</span><span class="sxs-lookup"><span data-stu-id="79b97-105">This property indicates the Windows product type.</span></span>

<span data-ttu-id="79b97-106">En el caso de los sistemas operativos Windows 2000 y versiones posteriores, el instalador establece los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="79b97-106">For Windows 2000 and later operating systems, the installer sets the following values.</span></span> <span data-ttu-id="79b97-107">Tenga en cuenta que los valores son los mismos que los del campo **wProductType** de la estructura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="79b97-107">Note that values are the same as of the **wProductType** field of the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span>



| <span data-ttu-id="79b97-108">Value</span><span class="sxs-lookup"><span data-stu-id="79b97-108">Value</span></span> | <span data-ttu-id="79b97-109">Significado</span><span class="sxs-lookup"><span data-stu-id="79b97-109">Meaning</span></span>                                  |
|-------|------------------------------------------|
| <span data-ttu-id="79b97-110">1</span><span class="sxs-lookup"><span data-stu-id="79b97-110">1</span></span>     | <span data-ttu-id="79b97-111">Windows 2000 Professional y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="79b97-111">Windows 2000 Professional and later</span></span>      |
| <span data-ttu-id="79b97-112">2</span><span class="sxs-lookup"><span data-stu-id="79b97-112">2</span></span>     | <span data-ttu-id="79b97-113">Controlador de dominio de Windows 2000 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="79b97-113">Windows 2000 domain controller and later</span></span> |
| <span data-ttu-id="79b97-114">3</span><span class="sxs-lookup"><span data-stu-id="79b97-114">3</span></span>     | <span data-ttu-id="79b97-115">Windows 2000 Server y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="79b97-115">Windows 2000 Server and later</span></span>            |



 

<span data-ttu-id="79b97-116">En el caso de sistemas operativos anteriores a Windows 2000, el instalador establece los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="79b97-116">For operating systems earlier than Windows 2000, the installer sets the following values.</span></span>



| <span data-ttu-id="79b97-117">Value</span><span class="sxs-lookup"><span data-stu-id="79b97-117">Value</span></span> | <span data-ttu-id="79b97-118">Significado</span><span class="sxs-lookup"><span data-stu-id="79b97-118">Meaning</span></span>                      |
|-------|------------------------------|
| <span data-ttu-id="79b97-119">1</span><span class="sxs-lookup"><span data-stu-id="79b97-119">1</span></span>     | <span data-ttu-id="79b97-120">Estación de trabajo Windows NT</span><span class="sxs-lookup"><span data-stu-id="79b97-120">Windows NT Workstation</span></span>       |
| <span data-ttu-id="79b97-121">2</span><span class="sxs-lookup"><span data-stu-id="79b97-121">2</span></span>     | <span data-ttu-id="79b97-122">Controlador de dominio de Windows NT</span><span class="sxs-lookup"><span data-stu-id="79b97-122">Windows NT domain controller</span></span> |
| <span data-ttu-id="79b97-123">3</span><span class="sxs-lookup"><span data-stu-id="79b97-123">3</span></span>     | <span data-ttu-id="79b97-124">Windows NT Server</span><span class="sxs-lookup"><span data-stu-id="79b97-124">Windows NT Server</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="79b97-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79b97-125">Requirements</span></span>



| <span data-ttu-id="79b97-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="79b97-126">Requirement</span></span> | <span data-ttu-id="79b97-127">Value</span><span class="sxs-lookup"><span data-stu-id="79b97-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79b97-128">Versión</span><span class="sxs-lookup"><span data-stu-id="79b97-128">Version</span></span><br/> | <span data-ttu-id="79b97-129">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="79b97-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="79b97-130">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="79b97-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="79b97-131">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="79b97-131">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="79b97-132">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="79b97-132">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79b97-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="79b97-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79b97-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79b97-134">Properties</span></span>](properties.md)
</dt> </dl>

 

 
