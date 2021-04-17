---
description: La propiedad PatchesEx devuelve un objeto RecordList que enumera la lista de revisiones.
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: Propiedad Installer. PatchesEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchesEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e615a9d17dbf1a40332afc5b49b3c0c5446963ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653387"
---
# <a name="installerpatchesex-property"></a><span data-ttu-id="a1575-103">Propiedad Installer. PatchesEx</span><span class="sxs-lookup"><span data-stu-id="a1575-103">Installer.PatchesEx property</span></span>

<span data-ttu-id="a1575-104">La propiedad **PatchesEx** devuelve un objeto [**RecordList**](recordlist-object.md) que enumera la lista de revisiones.</span><span class="sxs-lookup"><span data-stu-id="a1575-104">The **PatchesEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of patches.</span></span> <span data-ttu-id="a1575-105">Esta propiedad llama a [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span><span class="sxs-lookup"><span data-stu-id="a1575-105">This property calls [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span>

<span data-ttu-id="a1575-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a1575-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1575-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1575-107">Syntax</span></span>


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a><span data-ttu-id="a1575-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a1575-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a1575-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1575-109">Requirements</span></span>



| <span data-ttu-id="a1575-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1575-110">Requirement</span></span> | <span data-ttu-id="a1575-111">Value</span><span class="sxs-lookup"><span data-stu-id="a1575-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1575-112">Versión</span><span class="sxs-lookup"><span data-stu-id="a1575-112">Version</span></span><br/> | <span data-ttu-id="a1575-113">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a1575-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a1575-114">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a1575-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a1575-115">Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1575-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="a1575-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1575-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="a1575-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1575-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="a1575-118">IID</span><span class="sxs-lookup"><span data-stu-id="a1575-118">IID</span></span><br/>     | <span data-ttu-id="a1575-119">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a1575-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="a1575-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1575-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1575-121">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="a1575-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="a1575-122">**MsiEnumPatchesEx**</span><span class="sxs-lookup"><span data-stu-id="a1575-122">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="a1575-123">**Distribución**</span><span class="sxs-lookup"><span data-stu-id="a1575-123">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="a1575-124">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="a1575-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




