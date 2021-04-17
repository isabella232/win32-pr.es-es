---
description: El establecimiento de la propiedad DISABLEMEDIA evita que el instalador registre cualquier origen multimedia, como un CD-ROM, como un origen válido para el producto. Sin embargo, si la exploración está habilitada, es posible que un usuario siga explorando un origen de medios.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: Propiedad DISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670806"
---
# <a name="disablemedia-property"></a><span data-ttu-id="9ca9d-104">Propiedad DISABLEMEDIA</span><span class="sxs-lookup"><span data-stu-id="9ca9d-104">DISABLEMEDIA property</span></span>

<span data-ttu-id="9ca9d-105">El establecimiento de la propiedad [**DISABLEMEDIA**](disablemedia.md) evita que el instalador registre cualquier origen multimedia, como un CD-ROM, como un origen válido para el producto.</span><span class="sxs-lookup"><span data-stu-id="9ca9d-105">Setting the [**DISABLEMEDIA**](disablemedia.md) property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="9ca9d-106">Sin embargo, si la exploración está habilitada, es posible que un usuario siga explorando un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="9ca9d-106">If browsing is enabled, however, a user may still browse to a media source.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca9d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ca9d-107">Remarks</span></span>

<span data-ttu-id="9ca9d-108">Tenga en cuenta que la propiedad [**DISABLEMEDIA**](disablemedia.md) tiene un efecto diferente al establecimiento de la Directiva DISABLEMEDIA.</span><span class="sxs-lookup"><span data-stu-id="9ca9d-108">Note that the [**DISABLEMEDIA**](disablemedia.md) property has a different effect than setting the DisableMedia policy.</span></span> <span data-ttu-id="9ca9d-109">La configuración de **DISABLEMEDIA** impide el registro de cualquier origen multimedia y esto también evita la primera instalación de una aplicación desde un origen de medios.</span><span class="sxs-lookup"><span data-stu-id="9ca9d-109">Setting **DISABLEMEDIA** prevents the registration of any media source, and this also prevents the first time installation of an application from a media sources.</span></span>

<span data-ttu-id="9ca9d-110">Para obtener más información acerca de cómo proteger los orígenes de medios de la [*aplicación administrada*](m-gly.md) frente a la exploración e instalación por parte de usuarios no administrativos, consulte [resistencia de origen](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="9ca9d-110">For details about securing the media sources of [*managed application*](m-gly.md) against browsing and installation by non-administrative users, see [Source Resiliency](source-resiliency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca9d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ca9d-111">Requirements</span></span>



| <span data-ttu-id="9ca9d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ca9d-112">Requirement</span></span> | <span data-ttu-id="9ca9d-113">Value</span><span class="sxs-lookup"><span data-stu-id="9ca9d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca9d-114">Versión</span><span class="sxs-lookup"><span data-stu-id="9ca9d-114">Version</span></span><br/> | <span data-ttu-id="9ca9d-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9ca9d-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9ca9d-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9ca9d-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9ca9d-117">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9ca9d-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9ca9d-118">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9ca9d-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ca9d-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9ca9d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca9d-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9ca9d-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




