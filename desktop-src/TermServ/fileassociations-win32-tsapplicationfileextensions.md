---
title: Método FileAssociations de la clase Win32_TSApplicationFileExtensions
description: Examina el registro para obtener las asociaciones de archivo actuales para una aplicación.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Método FileAssociations Servicios de Escritorio remoto
- Método FileAssociations Servicios de Escritorio remoto, clase Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions de clase Servicios de Escritorio remoto, método FileAssociations
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686182"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="ed4cb-106">Método FileAssociations de la \_ clase TSApplicationFileExtensions de Win32</span><span class="sxs-lookup"><span data-stu-id="ed4cb-106">FileAssociations method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="ed4cb-107">Examina el registro para obtener las asociaciones de archivo actuales para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-107">Scans the registry to get the current file associations for an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed4cb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed4cb-108">Syntax</span></span>


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a><span data-ttu-id="ed4cb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed4cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed4cb-110">*AppPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ed4cb-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed4cb-111">Especifica la ruta de acceso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-111">Specifies the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="ed4cb-112">*FileAssociations* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ed4cb-112">*FileAssociations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed4cb-113">Al finalizar correctamente contiene las asociaciones de archivo para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-113">On successful completion contains the file associations for this application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed4cb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed4cb-114">Requirements</span></span>



| <span data-ttu-id="ed4cb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed4cb-115">Requirement</span></span> | <span data-ttu-id="ed4cb-116">Value</span><span class="sxs-lookup"><span data-stu-id="ed4cb-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4cb-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed4cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ed4cb-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ed4cb-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ed4cb-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed4cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ed4cb-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed4cb-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="ed4cb-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed4cb-121">Namespace</span></span><br/>                | <span data-ttu-id="ed4cb-122">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ed4cb-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ed4cb-123">MOF</span><span class="sxs-lookup"><span data-stu-id="ed4cb-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed4cb-124"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed4cb-124"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="ed4cb-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed4cb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed4cb-126"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed4cb-126"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed4cb-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed4cb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4cb-128">**Win32 \_ TSApplicationFileExtensions**</span><span class="sxs-lookup"><span data-stu-id="ed4cb-128">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> <dt>

[<span data-ttu-id="ed4cb-129">**Win32 \_ RDFileAssociation**</span><span class="sxs-lookup"><span data-stu-id="ed4cb-129">**Win32\_RDFileAssociation**</span></span>](win32-rdfileassociation.md)
</dt> </dl>

 

 





