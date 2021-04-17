---
description: El establecimiento de esta propiedad es como establecer la Directiva de directiva TransformsAtSource, excepto que el ámbito es diferente.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: Propiedad TRANSFORMSATSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681116"
---
# <a name="transformsatsource-property"></a><span data-ttu-id="83a87-103">Propiedad TRANSFORMSATSOURCE</span><span class="sxs-lookup"><span data-stu-id="83a87-103">TRANSFORMSATSOURCE property</span></span>

<span data-ttu-id="83a87-104">El establecimiento de esta propiedad es como establecer la Directiva de [Directiva TransformsAtSource](transformsatsource-policy.md) , excepto que el ámbito es diferente.</span><span class="sxs-lookup"><span data-stu-id="83a87-104">Setting this property is like setting the [TransformsAtSource policy](transformsatsource-policy.md) policy except that the scope is different.</span></span> <span data-ttu-id="83a87-105">La configuración de la Directiva TransformsAtSource se aplica a todos los paquetes instalados por un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="83a87-105">Setting TransformsAtSource policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="83a87-106">El establecimiento de la propiedad **TRANSFORMSATSOURCE** se aplica al paquete, independientemente de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="83a87-106">Setting the **TRANSFORMSATSOURCE** property applies to the package regardless of the users.</span></span>

## <a name="remarks"></a><span data-ttu-id="83a87-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83a87-107">Remarks</span></span>

<span data-ttu-id="83a87-108">Windows Installer interpreta la propiedad **TRANSFORMSATSOURCE** como si fuera la propiedad [**TRANSFORMSSECURE**](transformssecure.md) .</span><span class="sxs-lookup"><span data-stu-id="83a87-108">Windows Installer interprets the **TRANSFORMSATSOURCE** property as though it were the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="83a87-109">Si se pasa la marca @ en la propiedad [**TRANSformations**](transforms.md) , Windows Installer trata las transformaciones de la lista como [transformaciones seguras en el origen](secure-at-source-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="83a87-109">If the @ flag is passed in the [**TRANSFORMS**](transforms.md) property, Windows Installer treats the transforms in the list as [secure-at-source transforms](secure-at-source-transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83a87-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83a87-110">Requirements</span></span>



| <span data-ttu-id="83a87-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="83a87-111">Requirement</span></span> | <span data-ttu-id="83a87-112">Value</span><span class="sxs-lookup"><span data-stu-id="83a87-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83a87-113">Versión</span><span class="sxs-lookup"><span data-stu-id="83a87-113">Version</span></span><br/> | <span data-ttu-id="83a87-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="83a87-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="83a87-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="83a87-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="83a87-116">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="83a87-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="83a87-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="83a87-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83a87-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="83a87-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a87-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="83a87-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




