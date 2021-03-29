---
description: La propiedad State devuelve el estado de instalación de esta instancia de patch.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Patch. State (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653876"
---
# <a name="patchstate-property"></a><span data-ttu-id="0be4b-103">Patch. State (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0be4b-103">Patch.State property</span></span>

<span data-ttu-id="0be4b-104">La propiedad **State** devuelve el estado de instalación de esta instancia de patch.</span><span class="sxs-lookup"><span data-stu-id="0be4b-104">The **State** property returns the installation state of this instance of the patch.</span></span>

<span data-ttu-id="0be4b-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0be4b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be4b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0be4b-106">Syntax</span></span>


```JScript
propVal = Patch.State
```



## <a name="property-value"></a><span data-ttu-id="0be4b-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0be4b-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0be4b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0be4b-108">Remarks</span></span>

<span data-ttu-id="0be4b-109">Esta propiedad devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0be4b-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="0be4b-110">Estado de la instalación</span><span class="sxs-lookup"><span data-stu-id="0be4b-110">Installation State</span></span>        | <span data-ttu-id="0be4b-111">Significado</span><span class="sxs-lookup"><span data-stu-id="0be4b-111">Meaning</span></span>                                                      |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="0be4b-112">MSIPATCHSTATE \_ aplicado</span><span class="sxs-lookup"><span data-stu-id="0be4b-112">MSIPATCHSTATE\_APPLIED</span></span>    | <span data-ttu-id="0be4b-113">Patch se aplica a esta instancia del producto.</span><span class="sxs-lookup"><span data-stu-id="0be4b-113">Patch is applied to this product instance.</span></span>                   |
| <span data-ttu-id="0be4b-114">MSIPATCHSTATE \_ reemplazado</span><span class="sxs-lookup"><span data-stu-id="0be4b-114">MSIPATCHSTATE\_SUPERSEDED</span></span> | <span data-ttu-id="0be4b-115">Patch se aplica a esta instancia de producto, pero se reemplaza.</span><span class="sxs-lookup"><span data-stu-id="0be4b-115">Patch is applied to this product instance but is superseded.</span></span> |
| <span data-ttu-id="0be4b-116">MSIPATCHSTATE \_ obsoleto</span><span class="sxs-lookup"><span data-stu-id="0be4b-116">MSIPATCHSTATE\_OBSOLETED</span></span>  | <span data-ttu-id="0be4b-117">La revisión se aplica en esta instancia del producto pero está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="0be4b-117">Patch is applied in this product instance but obsolete.</span></span>      |



 

<span data-ttu-id="0be4b-118">Este método puede devolver ERROR \_ Unknown \_ patch si el objeto [**patch**](patch-object.md) se inicializa con una cadena vacía para *ProductCode*.</span><span class="sxs-lookup"><span data-stu-id="0be4b-118">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="0be4b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0be4b-119">Requirements</span></span>



| <span data-ttu-id="0be4b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0be4b-120">Requirement</span></span> | <span data-ttu-id="0be4b-121">Value</span><span class="sxs-lookup"><span data-stu-id="0be4b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0be4b-122">Versión</span><span class="sxs-lookup"><span data-stu-id="0be4b-122">Version</span></span><br/> | <span data-ttu-id="0be4b-123">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0be4b-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0be4b-124">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0be4b-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0be4b-125">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0be4b-125">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="0be4b-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0be4b-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="0be4b-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0be4b-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="0be4b-128">IID</span><span class="sxs-lookup"><span data-stu-id="0be4b-128">IID</span></span><br/>     | <span data-ttu-id="0be4b-129">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0be4b-129">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0be4b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0be4b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be4b-131">**Distribución**</span><span class="sxs-lookup"><span data-stu-id="0be4b-131">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="0be4b-132">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="0be4b-132">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="0be4b-133">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="0be4b-133">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




