---
title: Método Initialize INapEnforcementClientConnection (NapEnforcementClient. h)
description: Inicializa la conexión de cliente.
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Inicializar el método NAP
- Inicializar método NAP, interfaz INapEnforcementClientConnection
- Interfaz INapEnforcementClientConnection NAP, método Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51f12025bbddb8a9e795a97f2ed443344327a17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489886"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a><span data-ttu-id="a8b98-106">INapEnforcementClientConnection:: Initialize (método)</span><span class="sxs-lookup"><span data-stu-id="a8b98-106">INapEnforcementClientConnection::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="a8b98-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a8b98-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a8b98-108">El método **INapEnforcementClientConnection:: Initialize** inicializa la conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="a8b98-108">The **INapEnforcementClientConnection::Initialize** method initializes the client connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b98-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8b98-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="a8b98-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8b98-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b98-111">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a8b98-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b98-112">Un puntero a un [**EnforementEntityId**](nap-datatypes.md) que identifica el cliente de cumplimiento que solicita la conexión.</span><span class="sxs-lookup"><span data-stu-id="a8b98-112">A pointer to an [**EnforementEntityId**](nap-datatypes.md) that identifies the enforcement client requesting the connection.</span></span> <span data-ttu-id="a8b98-113">NapAgent establece este valor durante la creación de la conexión.</span><span class="sxs-lookup"><span data-stu-id="a8b98-113">This value is set by the NapAgent during connection creation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b98-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8b98-114">Return value</span></span>

<span data-ttu-id="a8b98-115">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="a8b98-115">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a8b98-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a8b98-116">Return code</span></span>                                                                                     | <span data-ttu-id="a8b98-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8b98-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a8b98-118"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="a8b98-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a8b98-119">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8b98-119">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a8b98-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a8b98-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a8b98-121">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="a8b98-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a8b98-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a8b98-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a8b98-123">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a8b98-123">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a8b98-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8b98-124">Requirements</span></span>



| <span data-ttu-id="a8b98-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b98-125">Requirement</span></span> | <span data-ttu-id="a8b98-126">Value</span><span class="sxs-lookup"><span data-stu-id="a8b98-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b98-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8b98-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b98-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a8b98-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a8b98-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8b98-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b98-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8b98-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a8b98-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8b98-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b98-132"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b98-132"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8b98-133">IDL</span><span class="sxs-lookup"><span data-stu-id="a8b98-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8b98-134"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8b98-134"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a8b98-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8b98-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8b98-136"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8b98-136"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a8b98-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8b98-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b98-138">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="a8b98-138">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





