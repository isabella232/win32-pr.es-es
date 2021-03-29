---
description: La propiedad ShortcutTarget del objeto de instalador examina un acceso directo y devuelve su producto, nombre de característica y componente si está disponible.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Propiedad Installer. ShortcutTarget
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653887"
---
# <a name="installershortcuttarget-property"></a><span data-ttu-id="9d8ed-103">Propiedad Installer. ShortcutTarget</span><span class="sxs-lookup"><span data-stu-id="9d8ed-103">Installer.ShortcutTarget property</span></span>

<span data-ttu-id="9d8ed-104">La propiedad **ShortcutTarget** del objeto de [**instalador**](installer-object.md) examina un acceso directo y devuelve su producto, nombre de característica y componente si está disponible.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-104">The **ShortcutTarget** property of the [**Installer**](installer-object.md) object examines a shortcut and returns its product, feature name, and component if available.</span></span>

<span data-ttu-id="9d8ed-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d8ed-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d8ed-106">Syntax</span></span>


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a><span data-ttu-id="9d8ed-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9d8ed-107">Property value</span></span>

<span data-ttu-id="9d8ed-108">Ruta de acceso completa y nombre de archivo para el archivo.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-108">Full path and file name for the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d8ed-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d8ed-109">Remarks</span></span>

<span data-ttu-id="9d8ed-110">ShortcutTarget devuelve un [**objeto de registro**](record-object.md) que contiene tres campos:</span><span class="sxs-lookup"><span data-stu-id="9d8ed-110">ShortcutTarget returns a [**Record object**](record-object.md) that contains three fields:</span></span>

-   <span data-ttu-id="9d8ed-111">El campo 1 es un GUID para el código de producto del acceso directo, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-111">Field 1 is a GUID for the product code of the shortcut, if available.</span></span> <span data-ttu-id="9d8ed-112">Este campo puede ser null.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-112">This field can be null.</span></span>
-   <span data-ttu-id="9d8ed-113">El campo 2 es el identificador de la característica del acceso directo, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-113">Field 2 is the Feature ID of the shortcut, if available.</span></span> <span data-ttu-id="9d8ed-114">Este campo puede ser null.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-114">This field can be null.</span></span>
-   <span data-ttu-id="9d8ed-115">El campo 3 es un GUID para el código del componente, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-115">Field 3 is a GUID for the component code, if available.</span></span> <span data-ttu-id="9d8ed-116">Este campo puede ser null.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-116">This field can be null.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d8ed-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d8ed-117">Requirements</span></span>



| <span data-ttu-id="9d8ed-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d8ed-118">Requirement</span></span> | <span data-ttu-id="9d8ed-119">Value</span><span class="sxs-lookup"><span data-stu-id="9d8ed-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d8ed-120">Versión</span><span class="sxs-lookup"><span data-stu-id="9d8ed-120">Version</span></span><br/> | <span data-ttu-id="9d8ed-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9d8ed-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9d8ed-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9d8ed-123">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d8ed-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9d8ed-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d8ed-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="9d8ed-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d8ed-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9d8ed-126">IID</span><span class="sxs-lookup"><span data-stu-id="9d8ed-126">IID</span></span><br/>     | <span data-ttu-id="9d8ed-127">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9d8ed-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="9d8ed-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d8ed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d8ed-129">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="9d8ed-129">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[<span data-ttu-id="9d8ed-130">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="9d8ed-130">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




