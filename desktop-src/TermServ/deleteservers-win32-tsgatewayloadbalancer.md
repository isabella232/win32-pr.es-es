---
title: Método DeleteServers de la clase Win32_TSGatewayLoadBalancer
description: Elimina los servidores de la propiedad servidores.
ms.assetid: 5ef44725-82b6-464a-abab-a68cc8799669
ms.tgt_platform: multiple
keywords:
- Método DeleteServers Servicios de Escritorio remoto
- Método DeleteServers Servicios de Escritorio remoto, clase Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de clase Servicios de Escritorio remoto, método DeleteServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b889f37b783853fbca0b9cb399a83959e2522d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422017"
---
# <a name="deleteservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="6f3cc-106">Método DeleteServers de la \_ clase TSGatewayLoadBalancer de Win32</span><span class="sxs-lookup"><span data-stu-id="6f3cc-106">DeleteServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="6f3cc-107">Elimina los servidores de la propiedad **servidores** .</span><span class="sxs-lookup"><span data-stu-id="6f3cc-107">Deletes servers from the **Servers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f3cc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f3cc-108">Syntax</span></span>


```mof
uint32 DeleteServers(
  [in] string Servers
);
```



## <a name="parameters"></a><span data-ttu-id="6f3cc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f3cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f3cc-110">*Servidores* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6f3cc-110">*Servers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f3cc-111">Lista separada por punto y coma de servidores de equilibrio de carga de puerta de enlace de escritorio remoto que se van a eliminar de la propiedad **servidores** .</span><span class="sxs-lookup"><span data-stu-id="6f3cc-111">Semicolon-separated list of RD Gateway load-balancing servers to delete from the **Servers** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f3cc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f3cc-112">Return value</span></span>

<span data-ttu-id="6f3cc-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="6f3cc-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6f3cc-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6f3cc-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6f3cc-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6f3cc-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f3cc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f3cc-116">Remarks</span></span>

<span data-ttu-id="6f3cc-117">Si hay varios servidores en el parámetro *Servers* y uno de ellos no se puede procesar, no se procesará ninguno de los servidores.</span><span class="sxs-lookup"><span data-stu-id="6f3cc-117">If multiple servers are in the *Servers* parameter and one of the servers cannot be processed, none of the servers will be processed.</span></span>

<span data-ttu-id="6f3cc-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="6f3cc-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6f3cc-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6f3cc-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6f3cc-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6f3cc-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6f3cc-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="6f3cc-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6f3cc-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6f3cc-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f3cc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f3cc-123">Requirements</span></span>



| <span data-ttu-id="6f3cc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f3cc-124">Requirement</span></span> | <span data-ttu-id="6f3cc-125">Value</span><span class="sxs-lookup"><span data-stu-id="6f3cc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f3cc-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f3cc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6f3cc-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6f3cc-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6f3cc-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f3cc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6f3cc-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f3cc-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6f3cc-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f3cc-130">Namespace</span></span><br/>                | <span data-ttu-id="6f3cc-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6f3cc-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6f3cc-132">MOF</span><span class="sxs-lookup"><span data-stu-id="6f3cc-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f3cc-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f3cc-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f3cc-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f3cc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f3cc-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f3cc-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6f3cc-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f3cc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f3cc-137">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="6f3cc-137">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

