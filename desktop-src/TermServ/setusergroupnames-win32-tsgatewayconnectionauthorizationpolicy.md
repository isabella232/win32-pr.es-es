---
title: Método SetUserGroupNames de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad UserGroupNames para esta Escritorio remoto Directiva de autorización de conexión (RD \ 160; CAP).
ms.assetid: 03c9b2c5-8769-46f2-941f-302d798dd3a1
ms.tgt_platform: multiple
keywords:
- Método SetUserGroupNames Servicios de Escritorio remoto
- Método SetUserGroupNames Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ca948b63cd106e7284b00c2c5f9e54c6dfa86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676922"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="96b8c-106">Método SetUserGroupNames de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="96b8c-106">SetUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="96b8c-107">Establece la propiedad **UserGroupNames** para esta escritorio remoto Directiva de autorización de conexión (Cap de RD).</span><span class="sxs-lookup"><span data-stu-id="96b8c-107">Sets the **UserGroupNames** property for this Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="96b8c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96b8c-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="96b8c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96b8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b8c-110">*UserGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96b8c-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96b8c-111">Lista de nombres de grupos de usuarios separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="96b8c-111">List of semicolon-separated user group names.</span></span> <span data-ttu-id="96b8c-112">Los nombres tienen el formato *dominio \\ UserGroupName*.</span><span class="sxs-lookup"><span data-stu-id="96b8c-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="96b8c-113">Si el usuario pertenece a alguno de estos grupos de usuarios, se le permitirá el acceso al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="96b8c-113">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b8c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96b8c-114">Return value</span></span>

<span data-ttu-id="96b8c-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="96b8c-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="96b8c-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="96b8c-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="96b8c-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="96b8c-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="96b8c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96b8c-118">Remarks</span></span>

<span data-ttu-id="96b8c-119">Si hay varios nombres de grupos de usuarios en el parámetro *UserGroupNames* y uno de los nombres no se puede procesar, no se procesará ninguno de los nombres.</span><span class="sxs-lookup"><span data-stu-id="96b8c-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="96b8c-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="96b8c-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="96b8c-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="96b8c-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="96b8c-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="96b8c-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="96b8c-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="96b8c-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="96b8c-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="96b8c-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="96b8c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96b8c-125">Requirements</span></span>



| <span data-ttu-id="96b8c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="96b8c-126">Requirement</span></span> | <span data-ttu-id="96b8c-127">Value</span><span class="sxs-lookup"><span data-stu-id="96b8c-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96b8c-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96b8c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="96b8c-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="96b8c-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="96b8c-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96b8c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="96b8c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96b8c-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="96b8c-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="96b8c-132">Namespace</span></span><br/>                | <span data-ttu-id="96b8c-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="96b8c-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="96b8c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="96b8c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96b8c-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96b8c-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="96b8c-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96b8c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96b8c-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96b8c-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="96b8c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="96b8c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b8c-139">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="96b8c-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

