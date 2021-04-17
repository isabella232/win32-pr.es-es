---
description: El método ExtractPatchXMLData del objeto de instalador extrae información de una revisión como una cadena XML. La información se puede utilizar para determinar si la revisión se aplica en un sistema de destino. Este método llama a MsiExtractPatchXMLData.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Instalador. ExtractPatchXMLData (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653352"
---
# <a name="installerextractpatchxmldata-method"></a><span data-ttu-id="6145e-105">Instalador. ExtractPatchXMLData (método)</span><span class="sxs-lookup"><span data-stu-id="6145e-105">Installer.ExtractPatchXMLData method</span></span>

<span data-ttu-id="6145e-106">El método **ExtractPatchXMLData** del objeto de [**instalador**](installer-object.md) extrae información de una revisión como una cadena XML.</span><span class="sxs-lookup"><span data-stu-id="6145e-106">The **ExtractPatchXMLData** method of the [**Installer**](installer-object.md) object extracts information from a patch as an XML string.</span></span> <span data-ttu-id="6145e-107">La información se puede utilizar para determinar si la revisión se aplica en un sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="6145e-107">The information can be used to determine whether the patch applies on a target system.</span></span> <span data-ttu-id="6145e-108">Este método llama a [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span><span class="sxs-lookup"><span data-stu-id="6145e-108">This method calls [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span>

## <a name="syntax"></a><span data-ttu-id="6145e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6145e-109">Syntax</span></span>


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a><span data-ttu-id="6145e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6145e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6145e-111">*PatchPath*</span><span class="sxs-lookup"><span data-stu-id="6145e-111">*PatchPath*</span></span> 
</dt> <dd>

<span data-ttu-id="6145e-112">Ruta de acceso completa a la revisión de la que se va a extraer la información de aplicabilidad.</span><span class="sxs-lookup"><span data-stu-id="6145e-112">Full path to the patch from which the applicability information is to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6145e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6145e-113">Return value</span></span>

<span data-ttu-id="6145e-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6145e-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6145e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6145e-115">Requirements</span></span>



| <span data-ttu-id="6145e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6145e-116">Requirement</span></span> | <span data-ttu-id="6145e-117">Value</span><span class="sxs-lookup"><span data-stu-id="6145e-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6145e-118">Versión</span><span class="sxs-lookup"><span data-stu-id="6145e-118">Version</span></span><br/> | <span data-ttu-id="6145e-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6145e-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6145e-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6145e-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6145e-121">Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6145e-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="6145e-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6145e-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6145e-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6145e-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="6145e-124">IID</span><span class="sxs-lookup"><span data-stu-id="6145e-124">IID</span></span><br/>     | <span data-ttu-id="6145e-125">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6145e-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="6145e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6145e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6145e-127">**MsiExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="6145e-127">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[<span data-ttu-id="6145e-128">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="6145e-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




