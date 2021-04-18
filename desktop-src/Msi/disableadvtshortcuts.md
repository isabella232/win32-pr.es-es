---
description: Al establecer la propiedad DISABLEADVTSHORTCUTS, se deshabilita la generación de accesos directos que admiten la instalación a petición y el anuncio. Al establecer esta propiedad, se especifica que estos métodos abreviados se deben reemplazar por métodos abreviados normales.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Propiedad DISABLEADVTSHORTCUTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653309"
---
# <a name="disableadvtshortcuts-property"></a><span data-ttu-id="7610d-104">Propiedad DISABLEADVTSHORTCUTS</span><span class="sxs-lookup"><span data-stu-id="7610d-104">DISABLEADVTSHORTCUTS property</span></span>

<span data-ttu-id="7610d-105">Al establecer la propiedad **DISABLEADVTSHORTCUTS** , se deshabilita la generación de accesos directos que admiten la [instalación a petición](installation-on-demand.md) y el [anuncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="7610d-105">Setting the **DISABLEADVTSHORTCUTS** property disables the generation of shortcuts supporting [installation-on-demand](installation-on-demand.md) and [advertisement](advertisement.md).</span></span> <span data-ttu-id="7610d-106">Al establecer esta propiedad, se especifica que estos métodos abreviados se deben reemplazar por métodos abreviados normales.</span><span class="sxs-lookup"><span data-stu-id="7610d-106">Setting this property specifies that these shortcuts should instead be replaced by regular shortcuts.</span></span>

## <a name="default-value"></a><span data-ttu-id="7610d-107">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7610d-107">Default Value</span></span>

<span data-ttu-id="7610d-108">De forma predeterminada, la generación de accesos directos de instalación a petición está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7610d-108">By default, installation-on-demand shortcut generation is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="7610d-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7610d-109">Remarks</span></span>

<span data-ttu-id="7610d-110">Los métodos abreviados que admiten el anuncio tienen el nombre de una característica, en lugar de una ruta de acceso de archivo con formato con el formato \[ \# filekey, que se \] escribe en la columna de destino de la [tabla de acceso directo](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="7610d-110">The shortcuts that support advertisement have the name of a feature, rather than a formatted file path of the form \[\#filekey\], entered in the Target column of the [Shortcut table](shortcut-table.md).</span></span> <span data-ttu-id="7610d-111">Si se establece esta propiedad y se instala la característica, el instalador genera un acceso directo normal a la característica.</span><span class="sxs-lookup"><span data-stu-id="7610d-111">If this property is set and the feature is installed, the installer generates a regular shortcut to the feature.</span></span>

<span data-ttu-id="7610d-112">Los administradores suelen usar esta propiedad para los usuarios que se desplazan entre los entornos que no admiten publicidad.</span><span class="sxs-lookup"><span data-stu-id="7610d-112">This property is commonly used by administrators for users who roam between environments that do and do not support advertising.</span></span> <span data-ttu-id="7610d-113">Esta propiedad se puede establecer mediante una transformación, en la secuencia administrativa o en la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="7610d-113">This property can be set by a transform, in the administrative stream, or in the [Property table](property-table.md).</span></span> <span data-ttu-id="7610d-114">Si se establece mediante la línea de comandos o mediante una llamada a [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), se debe restablecer de nuevo durante cada instalación posterior.</span><span class="sxs-lookup"><span data-stu-id="7610d-114">If it is set using the command line or by a call to [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), then it must be reset again during each subsequent installation.</span></span>

## <a name="requirements"></a><span data-ttu-id="7610d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7610d-115">Requirements</span></span>



| <span data-ttu-id="7610d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7610d-116">Requirement</span></span> | <span data-ttu-id="7610d-117">Value</span><span class="sxs-lookup"><span data-stu-id="7610d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7610d-118">Versión</span><span class="sxs-lookup"><span data-stu-id="7610d-118">Version</span></span><br/> | <span data-ttu-id="7610d-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7610d-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7610d-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7610d-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7610d-121">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7610d-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7610d-122">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7610d-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7610d-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7610d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7610d-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7610d-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




