---
description: La propiedad installed solo se establece si el producto se instala por equipo o para el usuario actual.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Propiedad installed
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653790"
---
# <a name="installed-property"></a><span data-ttu-id="5ed79-103">Propiedad installed</span><span class="sxs-lookup"><span data-stu-id="5ed79-103">Installed property</span></span>

<span data-ttu-id="5ed79-104">La propiedad **installed** solo se establece si el producto se instala por equipo o para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="5ed79-104">The **Installed** property is set only if the product is installed per-machine or for the current user.</span></span> <span data-ttu-id="5ed79-105">Esta propiedad no se establece si el producto está instalado para un usuario diferente.</span><span class="sxs-lookup"><span data-stu-id="5ed79-105">This property is not set if the product is installed for a different user.</span></span>

<span data-ttu-id="5ed79-106">La propiedad **installed** se puede usar en expresiones condicionales para determinar si un producto está instalado por equipo o para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="5ed79-106">The **Installed** property can be used in conditional expressions to determine whether a product is installed per-computer or for the current user.</span></span> <span data-ttu-id="5ed79-107">Por ejemplo, la propiedad se puede utilizar en la columna condicional de una tabla de secuencia o para diferenciar entre una instalación de primera instalación y otra de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="5ed79-107">For example, the property can be used in the conditional column of a sequence table or to differentiate between a first installation and a maintenance installation.</span></span>

<span data-ttu-id="5ed79-108">Para determinar si el producto está instalado para un usuario diferente, Compruebe la propiedad [**ProductState**](productstate.md) .</span><span class="sxs-lookup"><span data-stu-id="5ed79-108">To determine whether the product is installed for a different user, check the [**ProductState**](productstate.md) property.</span></span>

<span data-ttu-id="5ed79-109">El valor de la propiedad [**ProductVersion**](productversion.md) es la versión del producto en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="5ed79-109">The value of the [**ProductVersion**](productversion.md) property is the version of the product in string format.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed79-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ed79-110">Requirements</span></span>



| <span data-ttu-id="5ed79-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed79-111">Requirement</span></span> | <span data-ttu-id="5ed79-112">Value</span><span class="sxs-lookup"><span data-stu-id="5ed79-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed79-113">Versión</span><span class="sxs-lookup"><span data-stu-id="5ed79-113">Version</span></span><br/> | <span data-ttu-id="5ed79-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5ed79-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5ed79-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5ed79-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5ed79-116">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5ed79-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5ed79-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5ed79-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ed79-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5ed79-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed79-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5ed79-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




