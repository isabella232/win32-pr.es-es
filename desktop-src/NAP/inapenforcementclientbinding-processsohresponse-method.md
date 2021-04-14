---
title: Método INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient. h)
description: Lo usan los clientes de cumplimiento para procesar un SoHResponse cada vez que reciben un BLOB de datos SoHResponse del servidor de cumplimiento.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Método ProcessSoHResponse NAP
- Método ProcessSoHResponse NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535530"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a><span data-ttu-id="78fea-106">INapEnforcementClientBinding::P método rocessSoHResponse</span><span class="sxs-lookup"><span data-stu-id="78fea-106">INapEnforcementClientBinding::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="78fea-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="78fea-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="78fea-108">Los clientes de cumplimiento usan el método **INapEnforcementClientBinding::P rocesssohresponse** para procesar un SoHResponse cada vez que reciben un BLOB de datos SoHResponse del servidor de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="78fea-108">The **INapEnforcementClientBinding::ProcessSoHResponse** method is used by enforcement clients to process an SoHResponse whenever they receive an SoHResponse data blob from the enforcement server.</span></span>

## <a name="syntax"></a><span data-ttu-id="78fea-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78fea-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a><span data-ttu-id="78fea-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78fea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78fea-111">*conexión* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="78fea-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fea-112">Puntero COM a la interfaz [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) de la conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="78fea-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the client connection.</span></span> <span data-ttu-id="78fea-113">El NapAgent no conserva las referencias al objeto asociado a esta interfaz después de que se complete esta llamada al método.</span><span class="sxs-lookup"><span data-stu-id="78fea-113">The NapAgent does not hold references to the object associated with this interface after this method call completes.</span></span>

<span data-ttu-id="78fea-114">Debe usar una conexión establecida previamente para procesar los blobs de datos SOHResponse.</span><span class="sxs-lookup"><span data-stu-id="78fea-114">You must use a previously established connection for processing SOHResponse data blobs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78fea-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78fea-115">Return value</span></span>

<span data-ttu-id="78fea-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="78fea-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="78fea-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="78fea-117">Return code</span></span>                                                                                             | <span data-ttu-id="78fea-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="78fea-118">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="78fea-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="78fea-119"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="78fea-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="78fea-120">The operation is successful.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="78fea-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="78fea-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="78fea-122">No se han creado previamente conexiones en el cliente de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="78fea-122">No connections have previously been created on the enforcement client.</span></span> <br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="78fea-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="78fea-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="78fea-124">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="78fea-124">Permissions error, access denied.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="78fea-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="78fea-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="78fea-126">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="78fea-126">System resource limit, could not perform the operation.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="78fea-127"><dt>**\_paquete NAP E \_ no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="78fea-127"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl>  | <span data-ttu-id="78fea-128">Si se devuelve este valor, el cliente de cumplimiento debe quitar el paquete si NapAgent devuelve \_ un \_ paquete no válido de NAP \_ .</span><span class="sxs-lookup"><span data-stu-id="78fea-128">If this value is returned the enforcement client must drop the packet if the NapAgent returns NAP\_E\_INVALID\_PACKET.</span></span> <span data-ttu-id="78fea-129">En este caso, el exiginte debe asumir que el servidor al que se está comunicando no está habilitado para NAP y quitar la conexión de la lista activa (es decir, notificar a NapAgent de un estado de conexión inactivo).</span><span class="sxs-lookup"><span data-stu-id="78fea-129">In this case, the enforcer must assume that the server it is talking to is not NAP-enabled and remove the connection from the active list (i.e. notify the NapAgent of a connection state down).</span></span><br/> |
| <dl> <span data-ttu-id="78fea-130"><dt>**identificador de NAP \_ E no \_ coincidente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="78fea-130"><dt>**NAP\_E\_MISMATCHED\_ID**</dt></span></span> </dl>   | <span data-ttu-id="78fea-131">Si se devuelve este valor, indica que el identificador de correlación del paquete SoH-Response no coincidía con la respuesta de SoH pendiente.</span><span class="sxs-lookup"><span data-stu-id="78fea-131">If this value is returned it indicates that the correlation id in the SoH-Response packet did not match the outstanding SoH-Response.</span></span> <span data-ttu-id="78fea-132">En este caso, el exiginte debe quitar el paquete y esperar a otro paquete de SoH-Response más reciente.</span><span class="sxs-lookup"><span data-stu-id="78fea-132">In this case, the enforcer should drop the packet and wait for another newer SoH-Response packet.</span></span><br/> <span data-ttu-id="78fea-133">Esto puede deberse a una respuesta a un mensaje de solicitud anterior.</span><span class="sxs-lookup"><span data-stu-id="78fea-133">This may be caused by a response to an older request message.</span></span><br/>        |
| <dl> <span data-ttu-id="78fea-134"><dt>**NAP \_ E \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="78fea-134"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="78fea-135">El exigidor no se ha inicializado previamente.</span><span class="sxs-lookup"><span data-stu-id="78fea-135">The enforcer has not been previously initialized.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="78fea-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78fea-136">Remarks</span></span>

<span data-ttu-id="78fea-137">NapAgent consulta el BLOB de datos SoH-Response del objeto de conexión, lo procesa y establece la decisión resultante (por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="78fea-137">The NapAgent queries the SoH-Response data blob from the connection object, processes it, and sets the resulting decision (eg.</span></span> <span data-ttu-id="78fea-138">acceso completo/restringido/etc.) en el objeto de conexión.</span><span class="sxs-lookup"><span data-stu-id="78fea-138">full/restricted access/etc) on the connection object.</span></span>

<span data-ttu-id="78fea-139">El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="78fea-139">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="78fea-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78fea-140">Requirements</span></span>



| <span data-ttu-id="78fea-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="78fea-141">Requirement</span></span> | <span data-ttu-id="78fea-142">Value</span><span class="sxs-lookup"><span data-stu-id="78fea-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78fea-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78fea-143">Minimum supported client</span></span><br/> | <span data-ttu-id="78fea-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="78fea-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="78fea-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78fea-145">Minimum supported server</span></span><br/> | <span data-ttu-id="78fea-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="78fea-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="78fea-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78fea-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="78fea-148"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="78fea-148"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="78fea-149">IDL</span><span class="sxs-lookup"><span data-stu-id="78fea-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78fea-150"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78fea-150"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="78fea-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78fea-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78fea-152"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78fea-152"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="78fea-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="78fea-153">See also</span></span>

<dl> <span data-ttu-id="78fea-154"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="78fea-154"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="78fea-155">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="78fea-155">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="78fea-156">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="78fea-156">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





