---
title: Método GetLogEventName de la clase Win32_TSGatewayServerSettings
description: Devuelve el nombre del evento de registro para el índice de eventos de registro especificado.
ms.assetid: ca31ef8e-ab84-4132-a6d2-232b1e69230a
ms.tgt_platform: multiple
keywords:
- Método GetLogEventName Servicios de Escritorio remoto
- Método GetLogEventName Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método GetLogEventName
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetLogEventName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e9c608b7a12d3de48d75ecd5651df94d0267fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676825"
---
# <a name="getlogeventname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="3470f-106">Método GetLogEventName de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="3470f-106">GetLogEventName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="3470f-107">Devuelve el nombre del evento de registro para el índice de eventos de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="3470f-107">Returns the log event name for the specified log event index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3470f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3470f-108">Syntax</span></span>


```mof
uint32 GetLogEventName(
  [in]  uint32 EventIndex,
  [out] string EventName
);
```



## <a name="parameters"></a><span data-ttu-id="3470f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3470f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3470f-110">*EventIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3470f-110">*EventIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3470f-111">Índice del evento de registro.</span><span class="sxs-lookup"><span data-stu-id="3470f-111">Index of the log event.</span></span> <span data-ttu-id="3470f-112">El valor debe estar entre cero y el valor de la propiedad **MaxLogEvents** .</span><span class="sxs-lookup"><span data-stu-id="3470f-112">The value must be between zero and the value of the **MaxLogEvents** property.</span></span>

</dd> <dt>

<span data-ttu-id="3470f-113">*EventName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3470f-113">*EventName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3470f-114">Nombre del evento especificado.</span><span class="sxs-lookup"><span data-stu-id="3470f-114">Name of the specified event.</span></span> <span data-ttu-id="3470f-115">En la lista siguiente se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="3470f-115">The following list displays the possible values.</span></span>

<dt>

<span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>

<span data-ttu-id="3470f-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span><span class="sxs-lookup"><span data-stu-id="3470f-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span></span>


</dt> <dd>

<span data-ttu-id="3470f-117">El usuario se desconectó correctamente del recurso.</span><span class="sxs-lookup"><span data-stu-id="3470f-117">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>

<span data-ttu-id="3470f-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span><span class="sxs-lookup"><span data-stu-id="3470f-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="3470f-119">El usuario no pudo conectarse al recurso.</span><span class="sxs-lookup"><span data-stu-id="3470f-119">User failed to connect to the resource.</span></span>

</dd> <dt>

<span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="3470f-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="3470f-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="3470f-121">Error de autorización de conexión de usuario.</span><span class="sxs-lookup"><span data-stu-id="3470f-121">User failed connection authorization.</span></span>

</dd> <dt>

<span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="3470f-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="3470f-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="3470f-123">Error de autorización de recursos del usuario.</span><span class="sxs-lookup"><span data-stu-id="3470f-123">User failed resource authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>

<span data-ttu-id="3470f-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span><span class="sxs-lookup"><span data-stu-id="3470f-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="3470f-125">El usuario se conectó correctamente al recurso.</span><span class="sxs-lookup"><span data-stu-id="3470f-125">User successfully connected to the resource.</span></span>

</dd> <dt>

<span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="3470f-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="3470f-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="3470f-127">El usuario pasó correctamente la autorización de conexión.</span><span class="sxs-lookup"><span data-stu-id="3470f-127">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="3470f-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="3470f-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="3470f-129">El usuario ha pasado correctamente la autorización de recursos.</span><span class="sxs-lookup"><span data-stu-id="3470f-129">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3470f-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3470f-130">Return value</span></span>

<span data-ttu-id="3470f-131">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="3470f-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3470f-132">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="3470f-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3470f-133">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3470f-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3470f-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3470f-134">Remarks</span></span>

<span data-ttu-id="3470f-135">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="3470f-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3470f-136">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3470f-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3470f-137">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3470f-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3470f-138">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="3470f-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3470f-139">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3470f-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3470f-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3470f-140">Requirements</span></span>



| <span data-ttu-id="3470f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="3470f-141">Requirement</span></span> | <span data-ttu-id="3470f-142">Value</span><span class="sxs-lookup"><span data-stu-id="3470f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3470f-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3470f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3470f-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3470f-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3470f-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3470f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3470f-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3470f-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3470f-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3470f-147">Namespace</span></span><br/>                | <span data-ttu-id="3470f-148">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3470f-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3470f-149">MOF</span><span class="sxs-lookup"><span data-stu-id="3470f-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3470f-150"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3470f-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3470f-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3470f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3470f-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3470f-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3470f-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="3470f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3470f-154">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="3470f-154">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="3470f-155">**EnableLogEvent**</span><span class="sxs-lookup"><span data-stu-id="3470f-155">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="3470f-156">**IsLogEventEnabled**</span><span class="sxs-lookup"><span data-stu-id="3470f-156">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)
</dt> </dl>

 

