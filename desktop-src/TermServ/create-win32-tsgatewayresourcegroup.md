---
title: Método Create de la clase Win32_TSGatewayResourceGroup
description: Crea un grupo de recursos.
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create Method Servicios de Escritorio remoto, Win32_TSGatewayResourceGroup (clase)
- Win32_TSGatewayResourceGroup Servicios de Escritorio remoto de clase, Create (método)
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9c5179967c143faa36763b7a2aabb8849d2f13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079036"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="4e76e-106">Método Create de la \_ clase Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4e76e-106">Create method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="4e76e-107">Crea un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4e76e-107">Creates a resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e76e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e76e-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="4e76e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e76e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e76e-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4e76e-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e76e-111">Nombre del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4e76e-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="4e76e-112">*Descripción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4e76e-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e76e-113">Descripción del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4e76e-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="4e76e-114">*Recursos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4e76e-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e76e-115">Lista de recursos separados por punto y coma en este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4e76e-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="4e76e-116">Un " \* " hace referencia a todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="4e76e-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e76e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e76e-117">Return value</span></span>

<span data-ttu-id="4e76e-118">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="4e76e-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4e76e-119">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4e76e-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4e76e-120">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4e76e-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e76e-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e76e-121">Remarks</span></span>

<span data-ttu-id="4e76e-122">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="4e76e-122">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4e76e-123">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4e76e-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4e76e-124">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4e76e-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4e76e-125">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="4e76e-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4e76e-126">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4e76e-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e76e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e76e-127">Requirements</span></span>



| <span data-ttu-id="4e76e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e76e-128">Requirement</span></span> | <span data-ttu-id="4e76e-129">Value</span><span class="sxs-lookup"><span data-stu-id="4e76e-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e76e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e76e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4e76e-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4e76e-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4e76e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e76e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4e76e-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e76e-133">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4e76e-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4e76e-134">Namespace</span></span><br/>                | <span data-ttu-id="4e76e-135">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4e76e-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4e76e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="4e76e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e76e-137"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e76e-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e76e-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e76e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e76e-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e76e-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4e76e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e76e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e76e-141">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="4e76e-141">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

