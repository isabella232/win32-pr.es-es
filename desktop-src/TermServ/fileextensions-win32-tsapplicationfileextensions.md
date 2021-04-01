---
title: Método FileExtensions de la clase Win32_TSApplicationFileExtensions
description: Proporciona una lista de las extensiones de nombre de archivo controladas por una aplicación.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- Método FileExtensions Servicios de Escritorio remoto
- Método FileExtensions Servicios de Escritorio remoto, clase Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions de clase Servicios de Escritorio remoto, método FileExtensions
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996990"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="ee96e-106">Método FileExtensions de la \_ clase TSApplicationFileExtensions de Win32</span><span class="sxs-lookup"><span data-stu-id="ee96e-106">FileExtensions method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="ee96e-107">Proporciona una lista de las extensiones de nombre de archivo controladas por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ee96e-107">Provides a list of the file name extensions that are handled by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee96e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee96e-108">Syntax</span></span>


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a><span data-ttu-id="ee96e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee96e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee96e-110">*AppPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee96e-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee96e-111">Ruta de acceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ee96e-111">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="ee96e-112">*Extensiones* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ee96e-112">*Extensions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee96e-113">Extensiones de nombre de archivo controladas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ee96e-113">The file name extensions that are handled by the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee96e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee96e-114">Remarks</span></span>

<span data-ttu-id="ee96e-115">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="ee96e-115">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ee96e-116">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ee96e-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ee96e-117">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ee96e-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ee96e-118">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="ee96e-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ee96e-119">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ee96e-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee96e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee96e-120">Requirements</span></span>



| <span data-ttu-id="ee96e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee96e-121">Requirement</span></span> | <span data-ttu-id="ee96e-122">Value</span><span class="sxs-lookup"><span data-stu-id="ee96e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee96e-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee96e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ee96e-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ee96e-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ee96e-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee96e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ee96e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee96e-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee96e-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ee96e-127">Namespace</span></span><br/>                | <span data-ttu-id="ee96e-128">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ee96e-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ee96e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="ee96e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee96e-130"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee96e-130"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="ee96e-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee96e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee96e-132"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee96e-132"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee96e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee96e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee96e-134">**Win32 \_ TSApplicationFileExtensions**</span><span class="sxs-lookup"><span data-stu-id="ee96e-134">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

