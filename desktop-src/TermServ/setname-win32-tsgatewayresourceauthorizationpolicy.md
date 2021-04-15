---
title: Método SetName de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Establece la propiedad de nombre para la Escritorio remoto Directiva de autorización de recursos (RD \ 160; RAP).
ms.assetid: 3a652ece-11fe-4aa7-913d-39ef96ab1633
ms.tgt_platform: multiple
keywords:
- SetName (método) Servicios de Escritorio remoto
- Método SetName Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Clase Win32_TSGatewayResourceAuthorizationPolicy Servicios de Escritorio remoto, método SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7e595472302d97e91026b3a84dc466e248ef5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685978"
---
# <a name="setname-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="bd498-106">Método SetName de la \_ clase TSGatewayResourceAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="bd498-106">SetName method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="bd498-107">Establece la propiedad de **nombre** de la Directiva de autorización de recursos de escritorio remoto (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="bd498-107">Sets the **Name** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd498-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd498-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="bd498-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd498-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd498-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bd498-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd498-111">Nombre de la RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="bd498-111">Name of the RD RAP.</span></span> <span data-ttu-id="bd498-112">El nombre debe tener 64 caracteres o menos, único (se omite el caso) y no puede contener los siguientes caracteres reservados:</span><span class="sxs-lookup"><span data-stu-id="bd498-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="bd498-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="bd498-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="bd498-114">\*\[Pestaña\]</span><span class="sxs-lookup"><span data-stu-id="bd498-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd498-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd498-115">Return value</span></span>

<span data-ttu-id="bd498-116">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="bd498-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bd498-117">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bd498-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bd498-118">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bd498-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd498-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd498-119">Remarks</span></span>

<span data-ttu-id="bd498-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="bd498-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bd498-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bd498-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bd498-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bd498-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bd498-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="bd498-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bd498-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bd498-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd498-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd498-125">Requirements</span></span>



| <span data-ttu-id="bd498-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd498-126">Requirement</span></span> | <span data-ttu-id="bd498-127">Value</span><span class="sxs-lookup"><span data-stu-id="bd498-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd498-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd498-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bd498-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bd498-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bd498-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd498-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bd498-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd498-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bd498-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bd498-132">Namespace</span></span><br/>                | <span data-ttu-id="bd498-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bd498-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bd498-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bd498-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd498-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd498-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd498-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd498-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd498-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd498-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bd498-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd498-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd498-139">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="bd498-139">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

