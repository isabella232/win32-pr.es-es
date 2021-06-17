---
description: El instalador establece la propiedad VersionNT64 en el número de versión del sistema operativo solo si el sistema se ejecuta en un equipo de 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propiedad VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262077"
---
# <a name="versionnt64-property"></a><span data-ttu-id="58b40-103">Propiedad VersionNT64</span><span class="sxs-lookup"><span data-stu-id="58b40-103">VersionNT64 property</span></span>

<span data-ttu-id="58b40-104">El instalador establece la **propiedad VersionNT64** en el número de versión del sistema operativo solo si el sistema se ejecuta en un equipo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="58b40-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="58b40-105">La propiedad no está definida si el sistema operativo no es de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="58b40-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="58b40-106">El valor es un entero: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="58b40-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="58b40-107">Por motivos de compatibilidad, la propiedad [](template-summary.md) tampoco está definida si la propiedad Resumen de plantilla indica que el paquete es para sistemas Intel (x86) de 32 bits y el sistema operativo no puede ejecutar código Intel (x64) de 64 bits, como Windows 10 en ARM (ARM64).</span><span class="sxs-lookup"><span data-stu-id="58b40-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel (x86) systems and the operating system cannot run 64-bit Intel (x64) code, such as Windows 10 on ARM (ARM64).</span></span>

> [!NOTE]
> <span data-ttu-id="58b40-108">A partir Windows 10 compilación 21277, las compilaciones de ARM64 en el canal de desarrollo del programa Windows Insider Preview admiten aplicaciones x64.</span><span class="sxs-lookup"><span data-stu-id="58b40-108">As of Windows 10 Build 21277, ARM64 builds in the Dev channel of the Windows Insider Preview program have support for x64 applications.</span></span> <span data-ttu-id="58b40-109">En estas compilaciones arm64, la propiedad VersionNT64 se define para los paquetes x86.</span><span class="sxs-lookup"><span data-stu-id="58b40-109">On these ARM64 builds, the VersionNT64 property is defined for x86 packages.</span></span>

## <a name="remarks"></a><span data-ttu-id="58b40-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58b40-110">Remarks</span></span>

<span data-ttu-id="58b40-111">Las expresiones condicionales prueban Windows de 64 bits simplemente con el nombre de propiedad o comprobando la versión mediante un operador de comparación.</span><span class="sxs-lookup"><span data-stu-id="58b40-111">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="58b40-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58b40-112">Requirements</span></span>



| <span data-ttu-id="58b40-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="58b40-113">Requirement</span></span> | <span data-ttu-id="58b40-114">Valor</span><span class="sxs-lookup"><span data-stu-id="58b40-114">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58b40-115">Versión</span><span class="sxs-lookup"><span data-stu-id="58b40-115">Version</span></span><br/> | <span data-ttu-id="58b40-116">Windows Installer 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="58b40-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="58b40-117">Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="58b40-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="58b40-118">Windows Installer en Windows Server 2003 o Windows XP Consulte los requisitos de [Windows Installer Run-Time](windows-installer-portal.md) para obtener información sobre el Service Pack de Windows mínimo que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="58b40-118">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58b40-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="58b40-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58b40-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="58b40-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




