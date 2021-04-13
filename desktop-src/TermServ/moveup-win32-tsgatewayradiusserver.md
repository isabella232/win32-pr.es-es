---
title: Método MoveUp de la clase Win32_TSGatewayRADIUSServer
description: Mueve el servidor de Servicio de autenticación remota telefónica de usuario (RADIUS) una posición hacia arriba en el orden de prioridad.
ms.assetid: 060bb90d-72c0-4364-a44f-c6368434b174
ms.tgt_platform: multiple
keywords:
- MoveUp (método) Servicios de Escritorio remoto
- Método MoveUp Servicios de Escritorio remoto, clase Win32_TSGatewayRADIUSServer
- Clase Win32_TSGatewayRADIUSServer Servicios de Escritorio remoto, método MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca93eee44abd147576c6e678dce871ae4d49d921
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535314"
---
# <a name="moveup-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="2b8b9-106">Método MoveUp de la \_ clase TSGatewayRADIUSServer de Win32</span><span class="sxs-lookup"><span data-stu-id="2b8b9-106">MoveUp method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="2b8b9-107">Mueve el servidor de Servicio de autenticación remota telefónica de usuario (RADIUS) una posición hacia arriba en el orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-107">Moves this Remote Authentication Dial-In User Service (RADIUS) server one position up in the priority order.</span></span> <span data-ttu-id="2b8b9-108">Este método reduce la propiedad **Priority** del servidor RADIUS actual e incrementa la propiedad **Priority** del servidor RADIUS que precede al servidor RADIUS actual.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-108">This method decrements the **Priority** property of the current RADIUS server and increments the **Priority** property of the RADIUS server that precedes the current RADIUS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b8b9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b8b9-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="2b8b9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b8b9-110">Parameters</span></span>

<span data-ttu-id="2b8b9-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b8b9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b8b9-112">Return value</span></span>

<span data-ttu-id="2b8b9-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2b8b9-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2b8b9-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2b8b9-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2b8b9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b8b9-116">Remarks</span></span>

<span data-ttu-id="2b8b9-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2b8b9-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2b8b9-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2b8b9-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2b8b9-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2b8b9-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2b8b9-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b8b9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b8b9-122">Requirements</span></span>



| <span data-ttu-id="2b8b9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b8b9-123">Requirement</span></span> | <span data-ttu-id="2b8b9-124">Value</span><span class="sxs-lookup"><span data-stu-id="2b8b9-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8b9-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b8b9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2b8b9-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2b8b9-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2b8b9-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b8b9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2b8b9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b8b9-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2b8b9-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2b8b9-129">Namespace</span></span><br/>                | <span data-ttu-id="2b8b9-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2b8b9-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2b8b9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2b8b9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b8b9-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b8b9-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b8b9-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b8b9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b8b9-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b8b9-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2b8b9-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b8b9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b8b9-136">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="2b8b9-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

