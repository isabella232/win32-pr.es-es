---
title: Método IConnectionBrokerClient GetTargetInfo (Cbclient. h)
description: Solicita información sobre el equipo de destino al que se debe redirigir la conexión.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Método GetTargetInfo Servicios de Escritorio remoto
- Método GetTargetInfo Servicios de Escritorio remoto, interfaz IConnectionBrokerClient
- Interfaz IConnectionBrokerClient Servicios de Escritorio remoto, método GetTargetInfo
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533754"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a><span data-ttu-id="c1362-106">IConnectionBrokerClient:: GetTargetInfo (método)</span><span class="sxs-lookup"><span data-stu-id="c1362-106">IConnectionBrokerClient::GetTargetInfo method</span></span>

<span data-ttu-id="c1362-107">Solicita información sobre el equipo de destino al que se debe redirigir la conexión.</span><span class="sxs-lookup"><span data-stu-id="c1362-107">Requests information about the target computer where the connection should be redirected.</span></span> <span data-ttu-id="c1362-108">El redirector usa este método para obtener información de redirección de la solicitud de conexión entrante.</span><span class="sxs-lookup"><span data-stu-id="c1362-108">This method is used by the redirector to get redirection information for the incoming connection request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1362-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1362-109">Syntax</span></span>


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a><span data-ttu-id="c1362-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1362-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1362-111">*pConnectionInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1362-111">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1362-112">La dirección de una estructura de [**\_ \_ información de conexión CB**](cb-connection-info.md) que contiene información sobre la solicitud de conexión entrante.</span><span class="sxs-lookup"><span data-stu-id="c1362-112">The address of a [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure that contains information about the incoming connection request.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-113">*Reservado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1362-113">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1362-114">Este parámetro está reservado para un uso futuro y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c1362-114">This parameter is reserved for future use and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-115">*hStatusEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1362-115">*hStatusEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1362-116">Identificador de un evento que se establecerá cada vez que se actualice el progreso de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c1362-116">The handle of an event that will get set whenever there is an update to the progress of the request.</span></span> <span data-ttu-id="c1362-117">Usted es responsable de la creación y el cierre de este evento.</span><span class="sxs-lookup"><span data-stu-id="c1362-117">You are responsible for creating and closing this event.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-118">*pTargetInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c1362-118">*pTargetInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1362-119">Dirección de una estructura [**de \_ \_ información del destino CB**](cb-target-info.md) que recibe información sobre el equipo de destino al que se debe redirigir la conexión entrante.</span><span class="sxs-lookup"><span data-stu-id="c1362-119">The address of a [**CB\_TARGET\_INFO**](cb-target-info.md) structure that receives information about the target computer where the incoming connection should be redirected.</span></span> <span data-ttu-id="c1362-120">Dado que se trata de un método asincrónico, esta memoria debe permanecer disponible hasta que se complete la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c1362-120">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="c1362-121">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="c1362-121">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-122">*pResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c1362-122">*pResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1362-123">Dirección de una variable **DWORD** que recibe un código de resultado.</span><span class="sxs-lookup"><span data-stu-id="c1362-123">The address of a **DWORD** variable that receives a result code.</span></span> <span data-ttu-id="c1362-124">Dado que se trata de un método asincrónico, esta memoria debe permanecer disponible hasta que se complete la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c1362-124">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="c1362-125">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="c1362-125">For more information, see Remarks.</span></span>

<span data-ttu-id="c1362-126">Este código de resultado será uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="c1362-126">This result code will be one of the following values.</span></span>

<dt>

<span data-ttu-id="c1362-127">0</span><span class="sxs-lookup"><span data-stu-id="c1362-127">0</span></span>
</dt> <dd>

<span data-ttu-id="c1362-128">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c1362-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-129">0x0000400</span><span class="sxs-lookup"><span data-stu-id="c1362-129">0x0000400</span></span>
</dt> <dd>

<span data-ttu-id="c1362-130">No se pudo encontrar el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="c1362-130">The destination computer could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-131">0x0000401</span><span class="sxs-lookup"><span data-stu-id="c1362-131">0x0000401</span></span>
</dt> <dd>

<span data-ttu-id="c1362-132">El equipo de destino no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c1362-132">The destination computer is not available.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-133">0x0000402</span><span class="sxs-lookup"><span data-stu-id="c1362-133">0x0000402</span></span>
</dt> <dd>

<span data-ttu-id="c1362-134">Error al cargar el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="c1362-134">Error loading destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-135">0x0000403</span><span class="sxs-lookup"><span data-stu-id="c1362-135">0x0000403</span></span>
</dt> <dd>

<span data-ttu-id="c1362-136">Error al poner en conexión el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="c1362-136">Error bringing destination computer online.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-137">0x0000404</span><span class="sxs-lookup"><span data-stu-id="c1362-137">0x0000404</span></span>
</dt> <dd>

<span data-ttu-id="c1362-138">Error al redirigir al equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="c1362-138">Error redirecting to destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-139">0x0000405</span><span class="sxs-lookup"><span data-stu-id="c1362-139">0x0000405</span></span>
</dt> <dd>

<span data-ttu-id="c1362-140">Error al activar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1362-140">Error waking virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-141">0x0000406</span><span class="sxs-lookup"><span data-stu-id="c1362-141">0x0000406</span></span>
</dt> <dd>

<span data-ttu-id="c1362-142">Error al arrancar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1362-142">Error booting virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-143">0x0000407</span><span class="sxs-lookup"><span data-stu-id="c1362-143">0x0000407</span></span>
</dt> <dd>

<span data-ttu-id="c1362-144">Error al buscar la dirección IP de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1362-144">Error finding the IP address of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-145">0x0000408</span><span class="sxs-lookup"><span data-stu-id="c1362-145">0x0000408</span></span>
</dt> <dd>

<span data-ttu-id="c1362-146">El agente de sesión no encontró ningún equipo disponible en el grupo.</span><span class="sxs-lookup"><span data-stu-id="c1362-146">The session broker could not find any available computers in the pool.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-147">0x0000409</span><span class="sxs-lookup"><span data-stu-id="c1362-147">0x0000409</span></span>
</dt> <dd>

<span data-ttu-id="c1362-148">El agente de sesión canceló la conexión.</span><span class="sxs-lookup"><span data-stu-id="c1362-148">The session broker canceled the connection.</span></span>

</dd> <dt>

<span data-ttu-id="c1362-149">0x0000410</span><span class="sxs-lookup"><span data-stu-id="c1362-149">0x0000410</span></span>
</dt> <dd>

<span data-ttu-id="c1362-150">El agente de sesión no pudo validar la configuración de conexión.</span><span class="sxs-lookup"><span data-stu-id="c1362-150">The session broker could not validate the connection settings.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c1362-151">*ppCbReq* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c1362-151">*ppCbReq* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1362-152">Dirección de un puntero de interfaz [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) que se usa para obtener las actualizaciones de estado de una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c1362-152">The address of an [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) interface pointer that you use to obtain status updates for an asynchronous operation.</span></span> <span data-ttu-id="c1362-153">Esta interfaz se usa junto con el parámetro *hStatusEvent* para esperar y obtener los resultados de esta operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c1362-153">This interface is used in conjunction with the *hStatusEvent* parameter to wait for and get the results of this asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1362-154">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1362-154">Return value</span></span>

<span data-ttu-id="c1362-155">Devuelve **E \_ pendiente** si se crea la solicitud asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c1362-155">Returns **E\_PENDING** if the asynchronous request is created.</span></span> <span data-ttu-id="c1362-156">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1362-156">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1362-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1362-157">Remarks</span></span>

<span data-ttu-id="c1362-158">Este método es asincrónico.</span><span class="sxs-lookup"><span data-stu-id="c1362-158">This method is asynchronous.</span></span> <span data-ttu-id="c1362-159">Los parámetros *pTargetInfo* y *pResult* deben ser válidos hasta que el método [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) obtenga la **solicitud de \_ Estado CB \_ \_ completada**.</span><span class="sxs-lookup"><span data-stu-id="c1362-159">The *pTargetInfo* and *pResult* parameters must remain valid until the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method obtains **CB\_STATUS\_REQUEST\_COMPLETED**.</span></span>

<span data-ttu-id="c1362-160">Para obtener más información sobre cómo usar este método, consulte [Cómo usar la API de cliente de conexión a escritorio remoto Broker](use-the-remote-desktop-connection-broker-client-api.md).</span><span class="sxs-lookup"><span data-stu-id="c1362-160">For more information about how to use this method, see [How to use the Remote Desktop Connection Broker client API](use-the-remote-desktop-connection-broker-client-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1362-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1362-161">Requirements</span></span>



| <span data-ttu-id="c1362-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1362-162">Requirement</span></span> | <span data-ttu-id="c1362-163">Value</span><span class="sxs-lookup"><span data-stu-id="c1362-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1362-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1362-164">Minimum supported client</span></span><br/> | <span data-ttu-id="c1362-165">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c1362-165">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="c1362-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1362-166">Minimum supported server</span></span><br/> | <span data-ttu-id="c1362-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1362-167">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="c1362-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1362-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1362-169"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1362-169"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1362-170">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1362-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1362-171"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1362-171"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="c1362-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c1362-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1362-173"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1362-173"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1362-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1362-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1362-175">**IConnectionBrokerClient**</span><span class="sxs-lookup"><span data-stu-id="c1362-175">**IConnectionBrokerClient**</span></span>](iconnectionbrokerclient.md)
</dt> </dl>

 

 





