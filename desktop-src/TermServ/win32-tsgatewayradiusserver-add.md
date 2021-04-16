---
title: Método Add de la clase Win32_TSGatewayRADIUSServer
description: Agrega un nuevo servidor de Servicio de autenticación remota telefónica de usuario (RADIUS).
ms.assetid: 78f74bb6-8f70-4bc1-8e4d-1670a3ae3f31
ms.tgt_platform: multiple
keywords:
- Agregar método Servicios de Escritorio remoto
- Agregar método Servicios de Escritorio remoto, Win32_TSGatewayRADIUSServer interfaz
- Win32_TSGatewayRADIUSServer Servicios de Escritorio remoto de interfaz, método Add
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Add
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6869c55a6704944c34c68af065875cad92e8385c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676917"
---
# <a name="add-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="62882-106">Método Add de la \_ clase Win32 TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="62882-106">Add method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="62882-107">Agrega un nuevo servidor de Servicio de autenticación remota telefónica de usuario (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="62882-107">Adds a new Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="62882-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62882-108">Syntax</span></span>


```mof
uint32 Add(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="62882-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62882-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62882-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="62882-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62882-111">Nombre del servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="62882-111">RADIUS server name.</span></span>

</dd> <dt>

<span data-ttu-id="62882-112">*SharedSecret* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62882-112">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62882-113">Secreto compartido para el servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="62882-113">Shared secret for the RADIUS server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62882-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62882-114">Return value</span></span>

<span data-ttu-id="62882-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="62882-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="62882-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="62882-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="62882-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="62882-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62882-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62882-118">Remarks</span></span>

<span data-ttu-id="62882-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="62882-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="62882-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="62882-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="62882-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="62882-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="62882-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="62882-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="62882-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="62882-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="62882-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62882-124">Requirements</span></span>



| <span data-ttu-id="62882-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="62882-125">Requirement</span></span> | <span data-ttu-id="62882-126">Value</span><span class="sxs-lookup"><span data-stu-id="62882-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62882-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62882-127">Minimum supported client</span></span><br/> | <span data-ttu-id="62882-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="62882-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="62882-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62882-129">Minimum supported server</span></span><br/> | <span data-ttu-id="62882-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62882-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="62882-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="62882-131">Namespace</span></span><br/>                | <span data-ttu-id="62882-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="62882-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="62882-133">MOF</span><span class="sxs-lookup"><span data-stu-id="62882-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62882-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62882-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="62882-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62882-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62882-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62882-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="62882-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="62882-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62882-138">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="62882-138">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

