---
title: Método SetName de la clase Win32_TSGatewayResourceGroup
description: Establece la propiedad de nombre del grupo de recursos.
ms.assetid: 2c2fe1b6-5826-490e-aec2-479a0191e215
ms.tgt_platform: multiple
keywords:
- SetName (método) Servicios de Escritorio remoto
- Método SetName Servicios de Escritorio remoto, clase Win32_TSGatewayResourceGroup
- Clase Win32_TSGatewayResourceGroup Servicios de Escritorio remoto, método SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9ea16eb82896bb8fad67fff7ed849308100726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905248"
---
# <a name="setname-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="1aac8-106">Método SetName de la \_ clase TSGatewayResourceGroup de Win32</span><span class="sxs-lookup"><span data-stu-id="1aac8-106">SetName method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="1aac8-107">Establece la propiedad de **nombre** del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1aac8-107">Sets the **Name** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aac8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1aac8-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="1aac8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1aac8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aac8-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1aac8-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aac8-111">Nombre del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1aac8-111">Name of the resource group.</span></span> <span data-ttu-id="1aac8-112">El nombre debe tener 64 caracteres o menos, único (se omite el caso) y no puede contener los siguientes caracteres reservados:</span><span class="sxs-lookup"><span data-stu-id="1aac8-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="1aac8-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="1aac8-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="1aac8-114">\*\[Pestaña\]</span><span class="sxs-lookup"><span data-stu-id="1aac8-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aac8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1aac8-115">Return value</span></span>

<span data-ttu-id="1aac8-116">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="1aac8-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1aac8-117">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="1aac8-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1aac8-118">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1aac8-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1aac8-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1aac8-119">Remarks</span></span>

<span data-ttu-id="1aac8-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="1aac8-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1aac8-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1aac8-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1aac8-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1aac8-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1aac8-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="1aac8-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1aac8-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1aac8-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1aac8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1aac8-125">Requirements</span></span>



| <span data-ttu-id="1aac8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aac8-126">Requirement</span></span> | <span data-ttu-id="1aac8-127">Value</span><span class="sxs-lookup"><span data-stu-id="1aac8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aac8-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1aac8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1aac8-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1aac8-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1aac8-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1aac8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1aac8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1aac8-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1aac8-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1aac8-132">Namespace</span></span><br/>                | <span data-ttu-id="1aac8-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1aac8-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1aac8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1aac8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1aac8-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1aac8-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1aac8-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1aac8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aac8-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aac8-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1aac8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1aac8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aac8-139">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="1aac8-139">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

