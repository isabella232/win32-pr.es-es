---
title: IMsTscAxEvents OnRemoteProgramResult, método
description: Se llama cuando un programa RemoteApp devuelve un resultado al control de cliente.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- Método OnRemoteProgramResult Servicios de Escritorio remoto
- Método OnRemoteProgramResult Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRemoteProgramResult
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880e4fb3f6453114415f5bcc07a0afb9c176a1bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150497"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a><span data-ttu-id="57b44-106">IMsTscAxEvents:: OnRemoteProgramResult (método)</span><span class="sxs-lookup"><span data-stu-id="57b44-106">IMsTscAxEvents::OnRemoteProgramResult method</span></span>

<span data-ttu-id="57b44-107">Se llama cuando un programa RemoteApp devuelve un resultado al control de cliente.</span><span class="sxs-lookup"><span data-stu-id="57b44-107">Called when a RemoteApp program returns a result to the client control.</span></span>

## <a name="syntax"></a><span data-ttu-id="57b44-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57b44-108">Syntax</span></span>


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a><span data-ttu-id="57b44-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57b44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b44-110">*bstrRemoteProgram* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57b44-110">*bstrRemoteProgram* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57b44-111">Nombre del programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="57b44-111">The name of the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="57b44-112">*lError* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57b44-112">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57b44-113">El resultado del intento de iniciar el programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="57b44-113">The result of the attempt to launch the RemoteApp program.</span></span>

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span data-ttu-id="57b44-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="57b44-114"><span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="57b44-115">El programa RemoteApp se inició correctamente.</span><span class="sxs-lookup"><span data-stu-id="57b44-115">The RemoteApp program launched successfully.</span></span>

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span data-ttu-id="57b44-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="57b44-116"><span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="57b44-117">La sesión remota está bloqueada y no se puede iniciar el programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="57b44-117">The remote session is locked and the RemoteApp program cannot be launched.</span></span> <span data-ttu-id="57b44-118">El usuario debe escribir sus credenciales para desbloquear la sesión y, a continuación, iniciar el programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="57b44-118">The user must enter their credentials to unlock the session, and then launch the RemoteApp program.</span></span>

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span data-ttu-id="57b44-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="57b44-119"><span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="57b44-120">El programa RemoteApp devolvió un error de protocolo.</span><span class="sxs-lookup"><span data-stu-id="57b44-120">The RemoteApp program returned a protocol error.</span></span>

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span data-ttu-id="57b44-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0X3))</span><span class="sxs-lookup"><span data-stu-id="57b44-121"><span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="57b44-122">El programa RemoteApp no está en la lista aprobada del servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="57b44-122">The RemoteApp program is not in the approved list of the RD Session Host server.</span></span>

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span data-ttu-id="57b44-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="57b44-123"><span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="57b44-124">Se denegó la ruta de acceso de red al programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="57b44-124">The network path to the RemoteApp program was denied.</span></span>

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span data-ttu-id="57b44-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0X5))</span><span class="sxs-lookup"><span data-stu-id="57b44-125"><span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="57b44-126">No se encontró el archivo de programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="57b44-126">The RemoteApp program file was not found.</span></span>

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span data-ttu-id="57b44-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="57b44-127"><span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="57b44-128">No se pudo iniciar el programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="57b44-128">The RemoteApp program failed to launch.</span></span>

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span data-ttu-id="57b44-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0X7))</span><span class="sxs-lookup"><span data-stu-id="57b44-129"><span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0x7))</span></span>


</dt> <dd>

<span data-ttu-id="57b44-130">No se puede iniciar el programa RemoteApp porque la sesión muestra actualmente el escritorio seguro.</span><span class="sxs-lookup"><span data-stu-id="57b44-130">The RemoteApp program cannot be launched because the session is currently displaying the secure desktop.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="57b44-131">*vbIsExecutable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57b44-131">*vbIsExecutable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57b44-132">Indica si el programa RemoteApp se inició directamente, utilizando el nombre del archivo ejecutable o indirectamente, mediante una asociación de archivo.</span><span class="sxs-lookup"><span data-stu-id="57b44-132">Indicates whether the RemoteApp program was launched directly, by using the executable name or indirectly, by using a file association.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b44-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57b44-133">Return value</span></span>

<span data-ttu-id="57b44-134">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="57b44-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57b44-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57b44-135">Remarks</span></span>

<span data-ttu-id="57b44-136">Implemente este método en el receptor de eventos para recibir la notificación de que un programa RemoteApp devolvió un resultado.</span><span class="sxs-lookup"><span data-stu-id="57b44-136">Implement this method in your event sink to receive notification that a RemoteApp program returned a result.</span></span>

<span data-ttu-id="57b44-137">Se llama a este método inmediatamente después de que el control ActiveX intente iniciar el programa RemoteApp, y el parámetro *lError* indica el resultado del intento.</span><span class="sxs-lookup"><span data-stu-id="57b44-137">This method is called immediately after the ActiveX control attempts to launch the RemoteApp program, and the *lError* parameter indicates the result of the attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="57b44-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57b44-138">Requirements</span></span>



| <span data-ttu-id="57b44-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="57b44-139">Requirement</span></span> | <span data-ttu-id="57b44-140">Value</span><span class="sxs-lookup"><span data-stu-id="57b44-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57b44-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57b44-141">Minimum supported client</span></span><br/> | <span data-ttu-id="57b44-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="57b44-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="57b44-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57b44-143">Minimum supported server</span></span><br/> | <span data-ttu-id="57b44-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57b44-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="57b44-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="57b44-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="57b44-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57b44-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="57b44-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57b44-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57b44-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57b44-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="57b44-149">IID</span><span class="sxs-lookup"><span data-stu-id="57b44-149">IID</span></span><br/>                      | <span data-ttu-id="57b44-150">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="57b44-150">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="57b44-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="57b44-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b44-152">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="57b44-152">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





