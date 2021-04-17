---
description: El instalador establece la propiedad VersionNT en el número de versión del sistema operativo, sin definir si el sistema operativo no es Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 o Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Propiedad VersionNT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653670"
---
# <a name="versionnt-property"></a><span data-ttu-id="ea096-103">Propiedad VersionNT</span><span class="sxs-lookup"><span data-stu-id="ea096-103">VersionNT property</span></span>

<span data-ttu-id="ea096-104">El instalador establece la propiedad **VersionNT** en el número de versión del sistema operativo, sin definir si el sistema operativo no es Windows NT, Windows 2000, Windows XP, Windows Vista, windows Server 2008 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ea096-104">The installer sets the **VersionNT** property to the version number for the operating system, undefined if the operating system is not Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008, or Windows 7.</span></span> <span data-ttu-id="ea096-105">El valor es un entero: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="ea096-105">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="ea096-106">Las instrucciones condicionales que dependen del sistema operativo pueden utilizar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="ea096-106">Conditional statements that depend upon the operating system can use this property.</span></span>

<span data-ttu-id="ea096-107">Vea también [valores de propiedad del sistema operativo](operating-system-property-values.md).</span><span class="sxs-lookup"><span data-stu-id="ea096-107">See also [Operating System Property Values](operating-system-property-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea096-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea096-108">Remarks</span></span>

<span data-ttu-id="ea096-109">Las expresiones de condición pueden probar Windows NT, Windows 2000 o Windows XP con el nombre de la propiedad, o puede comprobar la versión mediante un operador de comparación.</span><span class="sxs-lookup"><span data-stu-id="ea096-109">Condition expressions can test for Windows NT, Windows 2000, or Windows XP by using the property name, or may verify the version by using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea096-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea096-110">Requirements</span></span>



| <span data-ttu-id="ea096-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea096-111">Requirement</span></span> | <span data-ttu-id="ea096-112">Value</span><span class="sxs-lookup"><span data-stu-id="ea096-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea096-113">Versión</span><span class="sxs-lookup"><span data-stu-id="ea096-113">Version</span></span><br/> | <span data-ttu-id="ea096-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ea096-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ea096-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea096-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ea096-116">Windows Installer en Windows Server 2003 o Windows XP, consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows necesaria para una versión de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ea096-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea096-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ea096-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea096-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea096-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




