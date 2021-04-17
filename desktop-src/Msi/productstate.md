---
description: El instalador establece la propiedad ProductState en el estado de instalación del producto en la inicialización.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Propiedad ProductState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681304"
---
# <a name="productstate-property"></a><span data-ttu-id="7e269-103">Propiedad ProductState</span><span class="sxs-lookup"><span data-stu-id="7e269-103">ProductState property</span></span>

<span data-ttu-id="7e269-104">El instalador establece la propiedad **ProductState** en el estado de instalación del producto en la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7e269-104">The installer sets the **ProductState** property to the installation state for the product at initialization.</span></span> <span data-ttu-id="7e269-105">Esta propiedad se establece en uno de los siguientes tipos de datos INSTALLSTATE devueltos por [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span><span class="sxs-lookup"><span data-stu-id="7e269-105">This property is set to one of the following INSTALLSTATE data types returned by [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span></span>



| <span data-ttu-id="7e269-106">INSTALLSTATE</span><span class="sxs-lookup"><span data-stu-id="7e269-106">INSTALLSTATE</span></span>             | <span data-ttu-id="7e269-107">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="7e269-107">Numeric value</span></span> | <span data-ttu-id="7e269-108">Estado de la instalación del producto</span><span class="sxs-lookup"><span data-stu-id="7e269-108">Installation state of product</span></span>                   |
|--------------------------|---------------|-------------------------------------------------|
| <span data-ttu-id="7e269-109">INSTALLSTATE \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="7e269-109">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="7e269-110">-1</span><span class="sxs-lookup"><span data-stu-id="7e269-110">-1</span></span>            | <span data-ttu-id="7e269-111">El producto no se anuncia ni se instala.</span><span class="sxs-lookup"><span data-stu-id="7e269-111">The product is neither advertised or installed.</span></span> |
| <span data-ttu-id="7e269-112">INSTALLSTATE \_ anunciado</span><span class="sxs-lookup"><span data-stu-id="7e269-112">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="7e269-113">1</span><span class="sxs-lookup"><span data-stu-id="7e269-113">1</span></span>             | <span data-ttu-id="7e269-114">El producto se anuncia pero no se instala.</span><span class="sxs-lookup"><span data-stu-id="7e269-114">The product is advertised but not installed.</span></span>    |
| <span data-ttu-id="7e269-115">INSTALLSTATE \_ ausente</span><span class="sxs-lookup"><span data-stu-id="7e269-115">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="7e269-116">2</span><span class="sxs-lookup"><span data-stu-id="7e269-116">2</span></span>             | <span data-ttu-id="7e269-117">El producto se instala para un usuario diferente.</span><span class="sxs-lookup"><span data-stu-id="7e269-117">The product is installed for a different user.</span></span>  |
| <span data-ttu-id="7e269-118">INSTALLSTATE ( \_ valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="7e269-118">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="7e269-119">5</span><span class="sxs-lookup"><span data-stu-id="7e269-119">5</span></span>             | <span data-ttu-id="7e269-120">El producto está instalado para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7e269-120">The product is installed for the current user.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="7e269-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e269-121">Requirements</span></span>



| <span data-ttu-id="7e269-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e269-122">Requirement</span></span> | <span data-ttu-id="7e269-123">Value</span><span class="sxs-lookup"><span data-stu-id="7e269-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e269-124">Versión</span><span class="sxs-lookup"><span data-stu-id="7e269-124">Version</span></span><br/> | <span data-ttu-id="7e269-125">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7e269-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7e269-126">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7e269-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7e269-127">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7e269-127">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7e269-128">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7e269-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e269-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7e269-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e269-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e269-130">Properties</span></span>](properties.md)
</dt> </dl>

 

 




