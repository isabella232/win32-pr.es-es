---
description: El establecimiento de la propiedad SHORTFILENAMES hace que se usen nombres de archivo cortos para los nombres de archivos de destino, en lugar de nombres de archivo largos. No afecta a los nombres de archivo que busca el instalador en el origen.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: SHORTFILENAMES (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654003"
---
# <a name="shortfilenames-property"></a><span data-ttu-id="ebc34-104">SHORTFILENAMES (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ebc34-104">SHORTFILENAMES property</span></span>

<span data-ttu-id="ebc34-105">El establecimiento de la propiedad **SHORTFILENAMES** hace que se usen nombres de archivo cortos para los nombres de archivos de destino, en lugar de nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="ebc34-105">Setting the **SHORTFILENAMES** property causes short file names to be used for the names of target files, rather than long file names.</span></span> <span data-ttu-id="ebc34-106">No afecta a los nombres de archivo que busca el instalador en el origen.</span><span class="sxs-lookup"><span data-stu-id="ebc34-106">It does not affect the file names the installer looks for at the source.</span></span>

## <a name="default-value"></a><span data-ttu-id="ebc34-107">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="ebc34-107">Default Value</span></span>

<span data-ttu-id="ebc34-108">El instalador usa nombres largos si no se establece la propiedad **SHORTFILENAMES** y el volumen de destino admite nombres largos.</span><span class="sxs-lookup"><span data-stu-id="ebc34-108">Long names are used by the installer if the **SHORTFILENAMES** property is not set and the target volume supports long names.</span></span> <span data-ttu-id="ebc34-109">El instalador usa nombres cortos si el volumen de destino no admite nombres largos.</span><span class="sxs-lookup"><span data-stu-id="ebc34-109">Short names are used by the installer if the target volume does not support long names.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebc34-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebc34-110">Remarks</span></span>

<span data-ttu-id="ebc34-111">Cuando se establece la propiedad **SHORTFILENAMES** , el instalador crea carpetas e instala archivos mediante nombres de archivo cortos a partir de los \| pares largos cortos enumerados en la tabla de [archivos](file-table.md) o en la [tabla de directorios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="ebc34-111">When the **SHORTFILENAMES** property is set, the installer creates folders and installs files using short file names from any short\|long pairs listed in the [File table](file-table.md) or [Directory table](directory-table.md).</span></span>

<span data-ttu-id="ebc34-112">Las aplicaciones pueden usar la función [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) para recuperar el formato de ruta de acceso abreviada de una ruta de acceso de archivo especificada.</span><span class="sxs-lookup"><span data-stu-id="ebc34-112">Applications can use the [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) function to retrieve the short path form of a specified file path.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebc34-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebc34-113">Requirements</span></span>



| <span data-ttu-id="ebc34-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebc34-114">Requirement</span></span> | <span data-ttu-id="ebc34-115">Value</span><span class="sxs-lookup"><span data-stu-id="ebc34-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc34-116">Versión</span><span class="sxs-lookup"><span data-stu-id="ebc34-116">Version</span></span><br/> | <span data-ttu-id="ebc34-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ebc34-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ebc34-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ebc34-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ebc34-119">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ebc34-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ebc34-120">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ebc34-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebc34-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ebc34-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc34-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ebc34-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 
