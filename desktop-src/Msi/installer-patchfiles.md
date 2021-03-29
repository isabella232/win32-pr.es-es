---
description: La propiedad PatchFiles devuelve un objeto StringList que contiene una lista de archivos que se pueden actualizar mediante la lista de revisiones proporcionada.
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: Propiedad Installer. PatchFiles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653965"
---
# <a name="installerpatchfiles-property"></a><span data-ttu-id="63c04-103">Propiedad Installer. PatchFiles</span><span class="sxs-lookup"><span data-stu-id="63c04-103">Installer.PatchFiles property</span></span>

<span data-ttu-id="63c04-104">La propiedad **PatchFiles** devuelve un objeto [**StringList**](stringlist-object.md) que contiene una lista de archivos que se pueden actualizar mediante la lista de revisiones proporcionada.</span><span class="sxs-lookup"><span data-stu-id="63c04-104">The **PatchFiles** property returns a [**StringList**](stringlist-object.md) object that contains a list of files that can be updated by the provided list of patches.</span></span> <span data-ttu-id="63c04-105">Esta propiedad llama a [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span><span class="sxs-lookup"><span data-stu-id="63c04-105">This property calls [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span></span> <span data-ttu-id="63c04-106">Para obtener más información acerca del uso de la propiedad **PatchFiles** , consulte [enumeración de los archivos que se pueden actualizar](listing-the-files-that-can-be-updated.md).</span><span class="sxs-lookup"><span data-stu-id="63c04-106">For more information about using the **PatchFiles** property see [Listing the Files that can be Updated](listing-the-files-that-can-be-updated.md).</span></span>

<span data-ttu-id="63c04-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="63c04-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c04-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63c04-108">Syntax</span></span>


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a><span data-ttu-id="63c04-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="63c04-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="63c04-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63c04-110">Requirements</span></span>



| <span data-ttu-id="63c04-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="63c04-111">Requirement</span></span> | <span data-ttu-id="63c04-112">Value</span><span class="sxs-lookup"><span data-stu-id="63c04-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63c04-113">Versión</span><span class="sxs-lookup"><span data-stu-id="63c04-113">Version</span></span><br/> | <span data-ttu-id="63c04-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="63c04-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="63c04-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="63c04-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="63c04-116">Windows Installer 4,5 en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="63c04-116">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="63c04-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63c04-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="63c04-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63c04-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="63c04-119">IID</span><span class="sxs-lookup"><span data-stu-id="63c04-119">IID</span></span><br/>     | <span data-ttu-id="63c04-120">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="63c04-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="63c04-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="63c04-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63c04-122">**Instalador (objeto)**</span><span class="sxs-lookup"><span data-stu-id="63c04-122">**Installer Object**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="63c04-123">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="63c04-123">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




