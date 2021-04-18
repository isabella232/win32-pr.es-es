---
description: El instalador establece la propiedad elemento uilevel en el nivel de la interfaz de usuario.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Propiedad elemento uilevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679557"
---
# <a name="uilevel-property"></a><span data-ttu-id="0b29b-103">Propiedad elemento uilevel</span><span class="sxs-lookup"><span data-stu-id="0b29b-103">UILevel property</span></span>

<span data-ttu-id="0b29b-104">El instalador establece la propiedad **elemento uilevel** en el nivel de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0b29b-104">The installer sets the **UILevel** property to the level of the user interface.</span></span> <span data-ttu-id="0b29b-105">La interfaz de usuario interna está habilitada y establecida por [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="0b29b-105">The internal UI is enabled and set by [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="0b29b-106">Esta propiedad se establece en uno de los siguientes tipos de datos INSTALLUILEVEL.</span><span class="sxs-lookup"><span data-stu-id="0b29b-106">This property is set to one of the following INSTALLUILEVEL data types.</span></span>



| <span data-ttu-id="0b29b-107">INSTALLUILEVEL</span><span class="sxs-lookup"><span data-stu-id="0b29b-107">INSTALLUILEVEL</span></span>          | <span data-ttu-id="0b29b-108">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="0b29b-108">Numeric value</span></span> | <span data-ttu-id="0b29b-109">Nivel de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="0b29b-109">User interface level</span></span>                        |
|-------------------------|---------------|---------------------------------------------|
| <span data-ttu-id="0b29b-110">INSTALLUILEVEL \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="0b29b-110">INSTALLUILEVEL\_NONE</span></span>    | <span data-ttu-id="0b29b-111">2</span><span class="sxs-lookup"><span data-stu-id="0b29b-111">2</span></span>             | <span data-ttu-id="0b29b-112">Instalación totalmente silenciosa.</span><span class="sxs-lookup"><span data-stu-id="0b29b-112">Completely silent installation.</span></span>             |
| <span data-ttu-id="0b29b-113">INSTALLUILEVEL \_ básico</span><span class="sxs-lookup"><span data-stu-id="0b29b-113">INSTALLUILEVEL\_BASIC</span></span>   | <span data-ttu-id="0b29b-114">3</span><span class="sxs-lookup"><span data-stu-id="0b29b-114">3</span></span>             | <span data-ttu-id="0b29b-115">Progreso simple y control de errores.</span><span class="sxs-lookup"><span data-stu-id="0b29b-115">Simple progress and error handling.</span></span>         |
| <span data-ttu-id="0b29b-116">INSTALLUILEVEL \_ reducido</span><span class="sxs-lookup"><span data-stu-id="0b29b-116">INSTALLUILEVEL\_REDUCED</span></span> | <span data-ttu-id="0b29b-117">4</span><span class="sxs-lookup"><span data-stu-id="0b29b-117">4</span></span>             | <span data-ttu-id="0b29b-118">Interfaz de usuario creada, se han suprimido los cuadros de diálogo del asistente.</span><span class="sxs-lookup"><span data-stu-id="0b29b-118">Authored UI, wizard dialogs suppressed.</span></span>     |
| <span data-ttu-id="0b29b-119">INSTALLUILEVEL \_ completo</span><span class="sxs-lookup"><span data-stu-id="0b29b-119">INSTALLUILEVEL\_FULL</span></span>    | <span data-ttu-id="0b29b-120">5</span><span class="sxs-lookup"><span data-stu-id="0b29b-120">5</span></span>             | <span data-ttu-id="0b29b-121">Interfaz de usuario creada con asistentes, progreso y errores.</span><span class="sxs-lookup"><span data-stu-id="0b29b-121">Authored UI with wizards, progress, errors.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0b29b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b29b-122">Requirements</span></span>



| <span data-ttu-id="0b29b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b29b-123">Requirement</span></span> | <span data-ttu-id="0b29b-124">Value</span><span class="sxs-lookup"><span data-stu-id="0b29b-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b29b-125">Versión</span><span class="sxs-lookup"><span data-stu-id="0b29b-125">Version</span></span><br/> | <span data-ttu-id="0b29b-126">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b29b-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0b29b-127">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0b29b-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0b29b-128">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0b29b-128">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0b29b-129">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0b29b-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b29b-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0b29b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b29b-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b29b-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="0b29b-132">Interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="0b29b-132">User Interface</span></span>](user-interface.md)
</dt> <dt>

[<span data-ttu-id="0b29b-133">Determinar el nivel de interfaz de usuario a partir de una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="0b29b-133">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




