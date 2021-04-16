---
description: La propiedad MSIARPSETTINGSIDENTIFIER contiene una lista delimitada por punto y coma de las ubicaciones del registro en las que la aplicación almacena las preferencias y la configuración de un usuario.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Propiedad MSIARPSETTINGSIDENTIFIER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671414"
---
# <a name="msiarpsettingsidentifier-property"></a><span data-ttu-id="afe56-103">Propiedad MSIARPSETTINGSIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="afe56-103">MSIARPSETTINGSIDENTIFIER property</span></span>

<span data-ttu-id="afe56-104">La propiedad **MSIARPSETTINGSIDENTIFIER** contiene una lista delimitada por punto y coma de las ubicaciones del registro en las que la aplicación almacena las preferencias y la configuración de un usuario.</span><span class="sxs-lookup"><span data-stu-id="afe56-104">The **MSIARPSETTINGSIDENTIFIER** property contains a semi-colon delimited list of the registry locations where the application stores a user's settings and preferences.</span></span> <span data-ttu-id="afe56-105">Durante una actualización del sistema operativo, el programa de instalación puede usar esta información para mejorar la experiencia de los usuarios que están migrando aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="afe56-105">During an operating system upgrade, setup can use this information to improve the experience of users who are migrating applications.</span></span>

<span data-ttu-id="afe56-106">El valor de la propiedad **MSIARPSETTINGSIDENTIFIER** es un texto literal que contiene la lista de ubicaciones del registro donde la aplicación almacena su configuración.</span><span class="sxs-lookup"><span data-stu-id="afe56-106">The value of the **MSIARPSETTINGSIDENTIFIER** property is literal text that contains the list of registry locations where the application stores its settings.</span></span> <span data-ttu-id="afe56-107">El valor puede especificar varias ubicaciones posibles del registro.</span><span class="sxs-lookup"><span data-stu-id="afe56-107">The value can specify multiple possible registry locations.</span></span> <span data-ttu-id="afe56-108">Separe varias ubicaciones del registro mediante punto y coma.</span><span class="sxs-lookup"><span data-stu-id="afe56-108">Separate multiple registry locations by using semi-colons.</span></span> <span data-ttu-id="afe56-109">La configuración de la aplicación normalmente se almacena en los subárboles del registro **HKCU** o **HKLM** de la forma: *\\ \\ versión* de la aplicación de empresa.</span><span class="sxs-lookup"><span data-stu-id="afe56-109">Application settings are typically stored in the **HKCU** or **HKLM** registry hives in the form: *Company\\Application\\Version*.</span></span> <span data-ttu-id="afe56-110">El ejemplo siguiente es un posible valor de la propiedad **MSIARPSETTINGSIDENTIFIER** .</span><span class="sxs-lookup"><span data-stu-id="afe56-110">The following example is a possible value for the **MSIARPSETTINGSIDENTIFIER** property.</span></span>

<span data-ttu-id="afe56-111">*Mycompany \\ AppSuite \\ 1,0; Mycompany \\ App1 \\ 1,0; Mycompany \\ App2 \\ 1,0*</span><span class="sxs-lookup"><span data-stu-id="afe56-111">*MyCompany\\AppSuite\\1.0;MyCompany\\App1\\1.0;MyCompany\\App2\\1.0*</span></span>

<span data-ttu-id="afe56-112">Esta propiedad es opcional y se puede establecer en la tabla de [propiedades](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="afe56-112">This property is optional and can be set in the [Property](property-table.md) table.</span></span> <span data-ttu-id="afe56-113">Si esta propiedad aparece en la tabla de propiedades, el valor no debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="afe56-113">If this property appears in the Property table, the value must not be set to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="afe56-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afe56-114">Requirements</span></span>



| <span data-ttu-id="afe56-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="afe56-115">Requirement</span></span> | <span data-ttu-id="afe56-116">Value</span><span class="sxs-lookup"><span data-stu-id="afe56-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afe56-117">Versión</span><span class="sxs-lookup"><span data-stu-id="afe56-117">Version</span></span><br/> | <span data-ttu-id="afe56-118">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="afe56-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="afe56-119">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="afe56-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="afe56-120">Windows Installer 4,5 en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="afe56-120">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="afe56-121">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="afe56-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="afe56-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="afe56-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe56-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="afe56-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="afe56-124">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="afe56-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




