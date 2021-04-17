---
description: La propiedad MediaDisks enumera todos los discos multimedia para esta instancia de producto. Esta propiedad llama a MsiSourceListEnumMediaDisks. Devuelve la información del disco como una matriz de objetos de registro.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Propiedad product. MediaDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e07af832837aaeb77759816c08cf68d04e14c255
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653424"
---
# <a name="productmediadisks-property"></a><span data-ttu-id="be7fa-105">Propiedad product. MediaDisks</span><span class="sxs-lookup"><span data-stu-id="be7fa-105">Product.MediaDisks property</span></span>

<span data-ttu-id="be7fa-106">La propiedad **MediaDisks** enumera todos los discos multimedia para esta instancia de producto.</span><span class="sxs-lookup"><span data-stu-id="be7fa-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="be7fa-107">Esta propiedad llama a [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span><span class="sxs-lookup"><span data-stu-id="be7fa-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="be7fa-108">Devuelve la información del disco como una matriz de objetos de [**registro**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="be7fa-108">Returns the disk information as an array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="be7fa-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="be7fa-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7fa-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be7fa-110">Syntax</span></span>


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="be7fa-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="be7fa-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="be7fa-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be7fa-112">Remarks</span></span>

<span data-ttu-id="be7fa-113">En cada registro, el primer campo contiene el ID. de disco, el segundo campo contiene la etiqueta de volumen y el tercer campo contiene el símbolo del sistema registrado para el disco.</span><span class="sxs-lookup"><span data-stu-id="be7fa-113">In each record, the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7fa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be7fa-114">Requirements</span></span>



| <span data-ttu-id="be7fa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7fa-115">Requirement</span></span> | <span data-ttu-id="be7fa-116">Value</span><span class="sxs-lookup"><span data-stu-id="be7fa-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be7fa-117">Versión</span><span class="sxs-lookup"><span data-stu-id="be7fa-117">Version</span></span><br/> | <span data-ttu-id="be7fa-118">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="be7fa-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="be7fa-119">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be7fa-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="be7fa-120">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="be7fa-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="be7fa-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be7fa-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="be7fa-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be7fa-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="be7fa-123">IID</span><span class="sxs-lookup"><span data-stu-id="be7fa-123">IID</span></span><br/>     | <span data-ttu-id="be7fa-124">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="be7fa-124">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="be7fa-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="be7fa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7fa-126">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="be7fa-126">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="be7fa-127">**MsiSourceListEnumMediaDisks**</span><span class="sxs-lookup"><span data-stu-id="be7fa-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="be7fa-128">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="be7fa-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




