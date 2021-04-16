---
description: El instalador establece la propiedad VersionNT64 en el número de versión del sistema operativo solo si el sistema se ejecuta en un equipo de 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propiedad VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679411"
---
# <a name="versionnt64-property"></a><span data-ttu-id="1a238-103">Propiedad VersionNT64</span><span class="sxs-lookup"><span data-stu-id="1a238-103">VersionNT64 property</span></span>

<span data-ttu-id="1a238-104">El instalador establece la propiedad **VersionNT64** en el número de versión del sistema operativo solo si el sistema se ejecuta en un equipo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1a238-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="1a238-105">Si el sistema operativo no es de 64 bits, la propiedad no está definida.</span><span class="sxs-lookup"><span data-stu-id="1a238-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="1a238-106">El valor es un entero: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="1a238-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="1a238-107">Por motivos de compatibilidad, la propiedad también está sin definir si la propiedad de Resumen de la [**plantilla**](template-summary.md) indica que el paquete es para los sistemas Intel de 32 bits y el sistema operativo es una arquitectura de 64 bits que no es Intel64 ni x64 (como ARM64).</span><span class="sxs-lookup"><span data-stu-id="1a238-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel systems and the operating system is a 64-bit architecture that is not Intel64 or x64 (such as ARM64).</span></span>

## <a name="remarks"></a><span data-ttu-id="1a238-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a238-108">Remarks</span></span>

<span data-ttu-id="1a238-109">Las expresiones condicionales prueban para Windows de 64 bits simplemente con el nombre de propiedad, o bien comprobando la versión con un operador de comparación.</span><span class="sxs-lookup"><span data-stu-id="1a238-109">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a238-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a238-110">Requirements</span></span>



| <span data-ttu-id="1a238-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a238-111">Requirement</span></span> | <span data-ttu-id="1a238-112">Value</span><span class="sxs-lookup"><span data-stu-id="1a238-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a238-113">Versión</span><span class="sxs-lookup"><span data-stu-id="1a238-113">Version</span></span><br/> | <span data-ttu-id="1a238-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1a238-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1a238-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1a238-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1a238-116">Windows Installer en Windows Server 2003 o Windows XP, consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows necesaria para una versión de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1a238-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a238-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1a238-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a238-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a238-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




