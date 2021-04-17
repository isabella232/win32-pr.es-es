---
description: La propiedad MediaDisks enumera todos los discos multimedia para esta instancia de producto. Esta propiedad llama a MsiSourceListEnumMediaDisks. Devuelve la información del disco como una matriz de objetos de registro.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Patch. MediaDisks (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653364"
---
# <a name="patchmediadisks-property"></a><span data-ttu-id="7e7f8-105">Patch. MediaDisks (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7e7f8-105">Patch.MediaDisks property</span></span>

<span data-ttu-id="7e7f8-106">La propiedad **MediaDisks** enumera todos los discos multimedia para esta instancia de producto.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="7e7f8-107">Esta propiedad llama a [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span><span class="sxs-lookup"><span data-stu-id="7e7f8-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="7e7f8-108">Devuelve la información del disco como una matriz de objetos de [**registro**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="7e7f8-108">Returns the disk information as array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="7e7f8-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7f8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e7f8-110">Syntax</span></span>


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="7e7f8-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7e7f8-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="7e7f8-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e7f8-112">Remarks</span></span>

<span data-ttu-id="7e7f8-113">En cada registro, el primer campo contiene el ID. de disco, el segundo campo contiene la etiqueta de volumen y el tercer campo contiene la solicitud de disco registrada para el disco.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-113">In each record the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e7f8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e7f8-114">Requirements</span></span>



| <span data-ttu-id="7e7f8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e7f8-115">Requirement</span></span> | <span data-ttu-id="7e7f8-116">Value</span><span class="sxs-lookup"><span data-stu-id="7e7f8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7f8-117">Versión</span><span class="sxs-lookup"><span data-stu-id="7e7f8-117">Version</span></span><br/> | <span data-ttu-id="7e7f8-118">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7e7f8-119">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7e7f8-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7e7f8-120">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7e7f8-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="7e7f8-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e7f8-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="7e7f8-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e7f8-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="7e7f8-123">IID</span><span class="sxs-lookup"><span data-stu-id="7e7f8-123">IID</span></span><br/>     | <span data-ttu-id="7e7f8-124">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7e7f8-124">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="7e7f8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e7f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7f8-126">**Distribución**</span><span class="sxs-lookup"><span data-stu-id="7e7f8-126">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="7e7f8-127">**MsiSourceListEnumMediaDisks**</span><span class="sxs-lookup"><span data-stu-id="7e7f8-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="7e7f8-128">**Record**</span><span class="sxs-lookup"><span data-stu-id="7e7f8-128">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="7e7f8-129">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="7e7f8-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




