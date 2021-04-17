---
description: El instalador establece la propiedad TempFolder en la ruta de acceso completa a la carpeta temporal. No es necesario que los autores establezcan la propiedad TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Propiedad TempFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653371"
---
# <a name="tempfolder-property"></a><span data-ttu-id="d2de8-103">Propiedad TempFolder</span><span class="sxs-lookup"><span data-stu-id="d2de8-103">TempFolder property</span></span>

<span data-ttu-id="d2de8-104">El instalador establece la propiedad **TempFolder** en la ruta de acceso completa a la carpeta temporal.</span><span class="sxs-lookup"><span data-stu-id="d2de8-104">The installer sets the **TempFolder** property to the full path to the Temp folder.</span></span>

<span data-ttu-id="d2de8-105">No es necesario que los autores establezcan la propiedad **TempFolder** .</span><span class="sxs-lookup"><span data-stu-id="d2de8-105">Authors should not need to set the **TempFolder** property.</span></span> <span data-ttu-id="d2de8-106">Windows Installer usa la función [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) para recuperar la ruta de acceso del directorio designado para los archivos temporales y establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d2de8-106">Windows Installer uses the [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files and to set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2de8-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2de8-107">Remarks</span></span>

<span data-ttu-id="d2de8-108">Un valor común para esta propiedad es C: \\ temp.</span><span class="sxs-lookup"><span data-stu-id="d2de8-108">A common value for this property is C:\\Temp.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2de8-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2de8-109">Requirements</span></span>



| <span data-ttu-id="d2de8-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2de8-110">Requirement</span></span> | <span data-ttu-id="d2de8-111">Value</span><span class="sxs-lookup"><span data-stu-id="d2de8-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2de8-112">Versión</span><span class="sxs-lookup"><span data-stu-id="d2de8-112">Version</span></span><br/> | <span data-ttu-id="d2de8-113">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d2de8-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d2de8-114">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d2de8-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d2de8-115">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d2de8-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d2de8-116">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d2de8-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2de8-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d2de8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2de8-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2de8-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 
