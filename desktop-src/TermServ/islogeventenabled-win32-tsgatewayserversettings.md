---
title: Método IsLogEventEnabled de la clase Win32_TSGatewayServerSettings
description: Indica si el tipo de registro de eventos especificado está habilitado.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- Método IsLogEventEnabled Servicios de Escritorio remoto
- Método IsLogEventEnabled Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método IsLogEventEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acefe60a9ba50c49146d25c7bccddf706f198c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686061"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="276e8-106">Método IsLogEventEnabled de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="276e8-106">IsLogEventEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="276e8-107">Indica si el tipo de registro de eventos especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="276e8-107">Indicates whether the specified event log type is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="276e8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="276e8-108">Syntax</span></span>


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="276e8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="276e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="276e8-110">*EventName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="276e8-110">*EventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="276e8-111">Nombre del tipo de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="276e8-111">Name of the event log type.</span></span> <span data-ttu-id="276e8-112">Este valor se debe recuperar mediante el método [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="276e8-112">This value should be retrieved by using the [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) method.</span></span>

<dt>

<span data-ttu-id="276e8-113">LogChannelDisconnect</span><span class="sxs-lookup"><span data-stu-id="276e8-113">LogChannelDisconnect</span></span>
</dt> <dd>

<span data-ttu-id="276e8-114">El usuario se desconectó correctamente del recurso.</span><span class="sxs-lookup"><span data-stu-id="276e8-114">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span data-ttu-id="276e8-115">LogFailedChannelConnect</span><span class="sxs-lookup"><span data-stu-id="276e8-115">LogFailedChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="276e8-116">El usuario no pudo conectarse al recurso.</span><span class="sxs-lookup"><span data-stu-id="276e8-116">User failed to connect to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="276e8-117">LogFailureNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="276e8-117">LogFailureNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="276e8-118">Error de autorización de conexión de usuario.</span><span class="sxs-lookup"><span data-stu-id="276e8-118">User failed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="276e8-119">LogFailureResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="276e8-119">LogFailureResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="276e8-120">Error de autorización de recursos del usuario.</span><span class="sxs-lookup"><span data-stu-id="276e8-120">User failed resource authorization.</span></span>

</dd> <dt>

<span data-ttu-id="276e8-121">LogSuccessChannelConnect</span><span class="sxs-lookup"><span data-stu-id="276e8-121">LogSuccessChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="276e8-122">El usuario se conectó correctamente al recurso.</span><span class="sxs-lookup"><span data-stu-id="276e8-122">User successfully connected to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="276e8-123">LogSuccessfulNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="276e8-123">LogSuccessfulNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="276e8-124">El usuario pasó correctamente la autorización de conexión.</span><span class="sxs-lookup"><span data-stu-id="276e8-124">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="276e8-125">LogSuccessfulResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="276e8-125">LogSuccessfulResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="276e8-126">El usuario ha pasado correctamente la autorización de recursos.</span><span class="sxs-lookup"><span data-stu-id="276e8-126">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="276e8-127">*Habilitado* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="276e8-127">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="276e8-128">Indica si el tipo de registro de eventos especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="276e8-128">Indicates whether the specified event log type is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="276e8-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="276e8-129">Return value</span></span>

<span data-ttu-id="276e8-130">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="276e8-130">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="276e8-131">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="276e8-131">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="276e8-132">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="276e8-132">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="276e8-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="276e8-133">Remarks</span></span>

<span data-ttu-id="276e8-134">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="276e8-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="276e8-135">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="276e8-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="276e8-136">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="276e8-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="276e8-137">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="276e8-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="276e8-138">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="276e8-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="276e8-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="276e8-139">Requirements</span></span>



| <span data-ttu-id="276e8-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="276e8-140">Requirement</span></span> | <span data-ttu-id="276e8-141">Value</span><span class="sxs-lookup"><span data-stu-id="276e8-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="276e8-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="276e8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="276e8-143">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="276e8-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="276e8-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="276e8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="276e8-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="276e8-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="276e8-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="276e8-146">Namespace</span></span><br/>                | <span data-ttu-id="276e8-147">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="276e8-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="276e8-148">MOF</span><span class="sxs-lookup"><span data-stu-id="276e8-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="276e8-149"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="276e8-149"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="276e8-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="276e8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="276e8-151"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="276e8-151"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="276e8-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="276e8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276e8-153">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="276e8-153">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="276e8-154">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="276e8-154">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

