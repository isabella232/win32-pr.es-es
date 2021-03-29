---
description: La propiedad ProductCode es un identificador único de la versión de producto determinada, representada como un GUID de cadena, por ejemplo &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: Propiedad ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680661"
---
# <a name="productcode-property"></a><span data-ttu-id="13409-103">Propiedad ProductCode</span><span class="sxs-lookup"><span data-stu-id="13409-103">ProductCode property</span></span>

<span data-ttu-id="13409-104">La propiedad **ProductCode** es un identificador único de la versión de producto determinada, representada como un [GUID](guid.md)de cadena, por ejemplo " {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="13409-104">The **ProductCode** property is a unique identifier for the particular product release, represented as a string [GUID](guid.md), for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="13409-105">Las letras usadas en este GUID deben estar en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="13409-105">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="13409-106">Este identificador debe variar en diferentes versiones e idiomas.</span><span class="sxs-lookup"><span data-stu-id="13409-106">This ID must vary for different versions and languages.</span></span>

<span data-ttu-id="13409-107">Una actualización de producto que actualice un producto en un producto completamente nuevo también debe cambiar el código de producto.</span><span class="sxs-lookup"><span data-stu-id="13409-107">A product upgrade that updates a product into an entirely new product must also change the product code.</span></span> <span data-ttu-id="13409-108">Las versiones de 32 bits y 64 bits del paquete de una aplicación deben tener asignados distintos códigos de producto.</span><span class="sxs-lookup"><span data-stu-id="13409-108">The 32-bit and 64-bit versions of an application's package must be assigned different product codes.</span></span>

<span data-ttu-id="13409-109">El **ProductCode** se anuncia como una propiedad del producto y es el método principal para especificar el producto.</span><span class="sxs-lookup"><span data-stu-id="13409-109">The **ProductCode** is advertised as a product property, and is the primary method of specifying the product.</span></span> <span data-ttu-id="13409-110">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="13409-110">This property is REQUIRED.</span></span>

## <a name="requirements"></a><span data-ttu-id="13409-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13409-111">Requirements</span></span>



| <span data-ttu-id="13409-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="13409-112">Requirement</span></span> | <span data-ttu-id="13409-113">Value</span><span class="sxs-lookup"><span data-stu-id="13409-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13409-114">Versión</span><span class="sxs-lookup"><span data-stu-id="13409-114">Version</span></span><br/> | <span data-ttu-id="13409-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="13409-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="13409-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13409-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="13409-117">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="13409-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="13409-118">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="13409-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="13409-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="13409-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13409-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13409-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




