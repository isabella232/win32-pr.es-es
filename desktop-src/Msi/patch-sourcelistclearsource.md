---
description: Quita un origen de red o dirección URL.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Patch. SourceListClearSource (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653436"
---
# <a name="patchsourcelistclearsource-method"></a><span data-ttu-id="ae8a2-103">Patch. SourceListClearSource (método)</span><span class="sxs-lookup"><span data-stu-id="ae8a2-103">Patch.SourceListClearSource method</span></span>

<span data-ttu-id="ae8a2-104">El método **SourceListClearSource** quita una red o un origen de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="ae8a2-104">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="ae8a2-105">Este método llama a [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span><span class="sxs-lookup"><span data-stu-id="ae8a2-105">This method calls [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae8a2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae8a2-106">Syntax</span></span>


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="ae8a2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae8a2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae8a2-108">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="ae8a2-108">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8a2-109">Tipo de origen que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="ae8a2-109">Type of source to be removed.</span></span>

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

<span data-ttu-id="ae8a2-110">**\_red MSISOURCETYPE**</span><span class="sxs-lookup"><span data-stu-id="ae8a2-110">**MSISOURCETYPE\_NETWORK**</span></span>
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

<span data-ttu-id="ae8a2-111">**\_dirección URL de MSISOURCETYPE**</span><span class="sxs-lookup"><span data-stu-id="ae8a2-111">**MSISOURCETYPE\_URL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="ae8a2-112">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="ae8a2-112">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8a2-113">Ruta de acceso al origen que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="ae8a2-113">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae8a2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae8a2-114">Return value</span></span>

<span data-ttu-id="ae8a2-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ae8a2-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae8a2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae8a2-116">Requirements</span></span>



| <span data-ttu-id="ae8a2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae8a2-117">Requirement</span></span> | <span data-ttu-id="ae8a2-118">Value</span><span class="sxs-lookup"><span data-stu-id="ae8a2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8a2-119">Versión</span><span class="sxs-lookup"><span data-stu-id="ae8a2-119">Version</span></span><br/> | <span data-ttu-id="ae8a2-120">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae8a2-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ae8a2-121">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ae8a2-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ae8a2-122">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ae8a2-122">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="ae8a2-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae8a2-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ae8a2-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae8a2-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="ae8a2-125">IID</span><span class="sxs-lookup"><span data-stu-id="ae8a2-125">IID</span></span><br/>     | <span data-ttu-id="ae8a2-126">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ae8a2-126">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="ae8a2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae8a2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae8a2-128">**Distribución**</span><span class="sxs-lookup"><span data-stu-id="ae8a2-128">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="ae8a2-129">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="ae8a2-129">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="ae8a2-130">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="ae8a2-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




