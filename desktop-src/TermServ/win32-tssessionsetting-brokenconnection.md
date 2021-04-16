---
title: Método BrokenConnection de la clase Win32_TSSessionSetting (Wtsprotocol. h)
description: Establece la propiedad BrokenConnectionAction, que es la acción que realiza el servidor si se alcanza el límite de tiempo de sesión o si se interrumpe la conexión.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Método BrokenConnection Servicios de Escritorio remoto
- Método BrokenConnection Servicios de Escritorio remoto, clase Win32_TSSessionSetting
- Win32_TSSessionSetting de clase Servicios de Escritorio remoto, método BrokenConnection
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685958"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="e2f4f-106">Método BrokenConnection de la \_ clase TSSessionSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="e2f4f-106">BrokenConnection method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="e2f4f-107">Establece la propiedad **BrokenConnectionAction** , que es la acción que realiza el servidor si se alcanza el límite de tiempo de sesión o si se interrumpe la conexión.</span><span class="sxs-lookup"><span data-stu-id="e2f4f-107">Sets the **BrokenConnectionAction** property, which is the action the server takes if the session time-limit is reached or if the connection is broken.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f4f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2f4f-108">Syntax</span></span>


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a><span data-ttu-id="e2f4f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2f4f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f4f-110">*BrokenConnectionAction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2f4f-110">*BrokenConnectionAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f4f-111">La acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="e2f4f-111">The action to take.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="e2f4f-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Desconectar** (0)</span><span class="sxs-lookup"><span data-stu-id="e2f4f-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e2f4f-113">El usuario se desconecta de la sesión.</span><span class="sxs-lookup"><span data-stu-id="e2f4f-113">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="e2f4f-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (1)</span><span class="sxs-lookup"><span data-stu-id="e2f4f-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e2f4f-115">La sesión se elimina permanentemente del servidor.</span><span class="sxs-lookup"><span data-stu-id="e2f4f-115">The session is permanently deleted from the server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f4f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2f4f-116">Return value</span></span>

<span data-ttu-id="e2f4f-117">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="e2f4f-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e2f4f-118">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e2f4f-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="e2f4f-119">El método devuelve un error si la configuración está en directiva de grupo control.</span><span class="sxs-lookup"><span data-stu-id="e2f4f-119">The method returns an error if the setting is under Group Policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f4f-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2f4f-120">Remarks</span></span>

<span data-ttu-id="e2f4f-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e2f4f-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e2f4f-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e2f4f-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e2f4f-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="e2f4f-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e2f4f-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e2f4f-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f4f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2f4f-125">Requirements</span></span>



| <span data-ttu-id="e2f4f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f4f-126">Requirement</span></span> | <span data-ttu-id="e2f4f-127">Value</span><span class="sxs-lookup"><span data-stu-id="e2f4f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f4f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2f4f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f4f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2f4f-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e2f4f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2f4f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f4f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2f4f-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e2f4f-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e2f4f-132">Namespace</span></span><br/>                | <span data-ttu-id="e2f4f-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e2f4f-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e2f4f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2f4f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2f4f-135"><dt>Wtsprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2f4f-135"><dt>Wtsprotocol.h</dt></span></span> </dl> |
| <span data-ttu-id="e2f4f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e2f4f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2f4f-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2f4f-137"><dt>TSCfgWmi.mof</dt></span></span> </dl>  |
| <span data-ttu-id="e2f4f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2f4f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2f4f-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2f4f-139"><dt>TSCfgWmi.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e2f4f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2f4f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f4f-141">**Win32 \_ TSSessionSetting**</span><span class="sxs-lookup"><span data-stu-id="e2f4f-141">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

