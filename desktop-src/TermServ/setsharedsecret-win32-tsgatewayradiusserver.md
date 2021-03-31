---
title: Método SetSharedSecret de la clase Win32_TSGatewayRADIUSServer
description: Establece la propiedad SharedSecret de este servidor Servicio de autenticación remota telefónica de usuario (RADIUS).
ms.assetid: b4f7afb7-862f-4c30-b60a-aa6a8dbbe3e9
ms.tgt_platform: multiple
keywords:
- Método SetSharedSecret Servicios de Escritorio remoto
- Método SetSharedSecret Servicios de Escritorio remoto, clase Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer de clase Servicios de Escritorio remoto, método SetSharedSecret
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetSharedSecret
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f17e22061467194bdb09fc3f2c6105706f58e587
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802924"
---
# <a name="setsharedsecret-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="65f04-106">Método SetSharedSecret de la \_ clase TSGatewayRADIUSServer de Win32</span><span class="sxs-lookup"><span data-stu-id="65f04-106">SetSharedSecret method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="65f04-107">Establece la propiedad **SharedSecret** de este servidor servicio de autenticación remota telefónica de usuario (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="65f04-107">Sets the **SharedSecret** property for this Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f04-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65f04-108">Syntax</span></span>


```mof
uint32 SetSharedSecret(
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="65f04-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65f04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f04-110">*SharedSecret* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65f04-110">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f04-111">Nuevo secreto compartido.</span><span class="sxs-lookup"><span data-stu-id="65f04-111">New shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f04-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65f04-112">Return value</span></span>

<span data-ttu-id="65f04-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="65f04-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="65f04-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="65f04-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="65f04-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="65f04-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="65f04-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65f04-116">Remarks</span></span>

<span data-ttu-id="65f04-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="65f04-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="65f04-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="65f04-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="65f04-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="65f04-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="65f04-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="65f04-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="65f04-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="65f04-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="65f04-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65f04-122">Requirements</span></span>



| <span data-ttu-id="65f04-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="65f04-123">Requirement</span></span> | <span data-ttu-id="65f04-124">Value</span><span class="sxs-lookup"><span data-stu-id="65f04-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f04-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65f04-125">Minimum supported client</span></span><br/> | <span data-ttu-id="65f04-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="65f04-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="65f04-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65f04-127">Minimum supported server</span></span><br/> | <span data-ttu-id="65f04-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65f04-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="65f04-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="65f04-129">Namespace</span></span><br/>                | <span data-ttu-id="65f04-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="65f04-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="65f04-131">MOF</span><span class="sxs-lookup"><span data-stu-id="65f04-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65f04-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65f04-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="65f04-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65f04-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65f04-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65f04-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="65f04-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="65f04-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f04-136">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="65f04-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

