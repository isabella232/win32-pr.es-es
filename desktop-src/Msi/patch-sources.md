---
description: La propiedad sources enumera todos los orígenes de la instancia patch. Esta propiedad llama a MsiSourceListEnumSources y devuelve una matriz de cadenas y acepta el tipo de origen como argumento.
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Patch. Sources (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18b9e6ab867d68908bc8dd7e7f87f942f8cd015c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653428"
---
# <a name="patchsources-property"></a><span data-ttu-id="95727-104">Patch. Sources (propiedad)</span><span class="sxs-lookup"><span data-stu-id="95727-104">Patch.Sources property</span></span>

<span data-ttu-id="95727-105">La propiedad **sources** enumera todos los orígenes de la instancia patch.</span><span class="sxs-lookup"><span data-stu-id="95727-105">The **Sources** property enumerates all the sources for the patch instance.</span></span> <span data-ttu-id="95727-106">Esta propiedad llama a [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) y devuelve una matriz de cadenas y acepta el tipo de origen como argumento.</span><span class="sxs-lookup"><span data-stu-id="95727-106">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns an array of strings, and accepts the source type as argument.</span></span>

<span data-ttu-id="95727-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="95727-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="95727-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95727-108">Syntax</span></span>


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a><span data-ttu-id="95727-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="95727-109">Property value</span></span>

<span data-ttu-id="95727-110">Tipo de origen que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="95727-110">The type of source to enumerate.</span></span> <span data-ttu-id="95727-111">El valor puede ser *msiInstallSourceTypeNetwork* (1) o *msiInstallSourceTypeURL* (2).</span><span class="sxs-lookup"><span data-stu-id="95727-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="95727-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95727-112">Requirements</span></span>



| <span data-ttu-id="95727-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="95727-113">Requirement</span></span> | <span data-ttu-id="95727-114">Value</span><span class="sxs-lookup"><span data-stu-id="95727-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95727-115">Versión</span><span class="sxs-lookup"><span data-stu-id="95727-115">Version</span></span><br/> | <span data-ttu-id="95727-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="95727-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="95727-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="95727-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="95727-118">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="95727-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="95727-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95727-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="95727-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95727-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="95727-121">IID</span><span class="sxs-lookup"><span data-stu-id="95727-121">IID</span></span><br/>     | <span data-ttu-id="95727-122">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="95727-122">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="95727-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="95727-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95727-124">**Distribución**</span><span class="sxs-lookup"><span data-stu-id="95727-124">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="95727-125">**MsiSourceListEnumSources**</span><span class="sxs-lookup"><span data-stu-id="95727-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="95727-126">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="95727-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




