---
title: Método AddComputerGroupNames de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Agrega los nombres de grupo de equipos especificados a la propiedad ComputerGroupNames.
ms.assetid: f0c440d6-0cc2-48b4-b656-65f12e652151
ms.tgt_platform: multiple
keywords:
- Método AddComputerGroupNames Servicios de Escritorio remoto
- Método AddComputerGroupNames Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método AddComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72647ef66b9e2eeaed824b3e77c404214786b615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150506"
---
# <a name="addcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="66702-106">Método AddComputerGroupNames de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="66702-106">AddComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="66702-107">Agrega los nombres de grupo de equipos especificados a la propiedad **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="66702-107">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="66702-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66702-108">Syntax</span></span>


```mof
uint32 AddComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="66702-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66702-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66702-110">*ComputerGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66702-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66702-111">Lista separada por puntos y comas de nombres de grupos de equipos que se van a agregar a la propiedad **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="66702-111">Semicolon-separated list of computer group names to add to the **ComputerGroupNames** property.</span></span> <span data-ttu-id="66702-112">Los nombres de los grupos de equipos deben tener el formato *dominio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="66702-112">Computer group names should be of the format *Domain\\ComputerGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66702-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66702-113">Return value</span></span>

<span data-ttu-id="66702-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="66702-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="66702-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="66702-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="66702-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="66702-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="66702-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66702-117">Remarks</span></span>

<span data-ttu-id="66702-118">Si hay varios nombres de grupos de equipos en el parámetro *ComputerGroupNames* y uno de los nombres no se puede procesar, no se procesará ninguno de los nombres.</span><span class="sxs-lookup"><span data-stu-id="66702-118">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="66702-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="66702-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="66702-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="66702-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="66702-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="66702-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="66702-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="66702-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="66702-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="66702-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="66702-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66702-124">Requirements</span></span>



| <span data-ttu-id="66702-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="66702-125">Requirement</span></span> | <span data-ttu-id="66702-126">Value</span><span class="sxs-lookup"><span data-stu-id="66702-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66702-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66702-127">Minimum supported client</span></span><br/> | <span data-ttu-id="66702-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="66702-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="66702-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66702-129">Minimum supported server</span></span><br/> | <span data-ttu-id="66702-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66702-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="66702-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="66702-131">Namespace</span></span><br/>                | <span data-ttu-id="66702-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="66702-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="66702-133">MOF</span><span class="sxs-lookup"><span data-stu-id="66702-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66702-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66702-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="66702-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66702-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66702-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66702-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="66702-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="66702-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66702-138">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="66702-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

