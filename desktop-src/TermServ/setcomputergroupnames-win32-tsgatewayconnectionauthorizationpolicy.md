---
title: Método SetComputerGroupNames de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad ComputerGroupNames.
ms.assetid: dd6747df-140f-4eeb-857b-d14f8713586c
ms.tgt_platform: multiple
keywords:
- Método SetComputerGroupNames Servicios de Escritorio remoto
- Método SetComputerGroupNames Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99c29ce37aeb8bfad0ae77197c7364b0135fa99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422266"
---
# <a name="setcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="ac115-106">Método SetComputerGroupNames de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="ac115-106">SetComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="ac115-107">Establece la propiedad **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="ac115-107">Sets the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac115-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac115-108">Syntax</span></span>


```mof
uint32 SetComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="ac115-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac115-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac115-110">*ComputerGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac115-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac115-111">Lista de nombres de grupos de equipos separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="ac115-111">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="ac115-112">Este valor puede estar vacío.</span><span class="sxs-lookup"><span data-stu-id="ac115-112">This value can be empty.</span></span> <span data-ttu-id="ac115-113">Los nombres tienen el formato *dominio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="ac115-113">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="ac115-114">Si se especifica un valor, el equipo cliente debe pertenecer a uno de estos grupos de equipos para que el usuario tenga acceso al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ac115-114">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac115-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac115-115">Return value</span></span>

<span data-ttu-id="ac115-116">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="ac115-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ac115-117">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="ac115-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ac115-118">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ac115-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac115-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac115-119">Remarks</span></span>

<span data-ttu-id="ac115-120">Si hay varios nombres de grupos de equipos en el parámetro *ComputerGroupNames* y uno de los nombres no se puede procesar, no se procesará ninguno de los nombres.</span><span class="sxs-lookup"><span data-stu-id="ac115-120">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="ac115-121">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="ac115-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ac115-122">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ac115-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ac115-123">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ac115-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ac115-124">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="ac115-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ac115-125">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ac115-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac115-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac115-126">Requirements</span></span>



| <span data-ttu-id="ac115-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac115-127">Requirement</span></span> | <span data-ttu-id="ac115-128">Value</span><span class="sxs-lookup"><span data-stu-id="ac115-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac115-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac115-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ac115-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ac115-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ac115-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac115-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ac115-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac115-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ac115-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ac115-133">Namespace</span></span><br/>                | <span data-ttu-id="ac115-134">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ac115-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ac115-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ac115-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac115-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac115-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac115-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac115-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac115-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac115-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ac115-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac115-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac115-140">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="ac115-140">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

