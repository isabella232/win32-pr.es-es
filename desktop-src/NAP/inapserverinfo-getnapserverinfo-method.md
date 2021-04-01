---
title: Método INapServerInfo GetNapServerInfo (NapServerManagement. h)
description: Recupera información acerca del servidor NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- Método GetNapServerInfo NAP
- Método GetNapServerInfo NAP, interfaz INapServerInfo
- Interfaz INapServerInfo NAP, método GetNapServerInfo
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804064"
---
# <a name="inapserverinfogetnapserverinfo-method"></a><span data-ttu-id="0921c-106">INapServerInfo:: GetNapServerInfo (método)</span><span class="sxs-lookup"><span data-stu-id="0921c-106">INapServerInfo::GetNapServerInfo method</span></span>

> [!Note]  
> <span data-ttu-id="0921c-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0921c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0921c-108">El método **INapServerInfo:: GetNapServerInfo** recupera información sobre el servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="0921c-108">The **INapServerInfo::GetNapServerInfo** method retrieves information about the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0921c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0921c-109">Syntax</span></span>


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="0921c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0921c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0921c-111">*nombreDeServidor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0921c-111">*serverName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0921c-112">Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="0921c-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server name.</span></span>

</dd> <dt>

<span data-ttu-id="0921c-113">*serverDescription* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0921c-113">*serverDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0921c-114">Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la descripción del servidor.</span><span class="sxs-lookup"><span data-stu-id="0921c-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server description.</span></span>

</dd> <dt>

<span data-ttu-id="0921c-115">*protocolVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0921c-115">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0921c-116">Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene la versión del protocolo.</span><span class="sxs-lookup"><span data-stu-id="0921c-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0921c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0921c-117">Return value</span></span>

<span data-ttu-id="0921c-118">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="0921c-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0921c-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0921c-119">Return code</span></span>                                                                                     | <span data-ttu-id="0921c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0921c-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0921c-121"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="0921c-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0921c-122">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="0921c-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0921c-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0921c-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0921c-124">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="0921c-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0921c-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0921c-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0921c-126">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="0921c-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0921c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0921c-127">Requirements</span></span>



| <span data-ttu-id="0921c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0921c-128">Requirement</span></span> | <span data-ttu-id="0921c-129">Value</span><span class="sxs-lookup"><span data-stu-id="0921c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0921c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0921c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0921c-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0921c-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="0921c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0921c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0921c-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0921c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0921c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0921c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0921c-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="0921c-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="0921c-136">IDL</span><span class="sxs-lookup"><span data-stu-id="0921c-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0921c-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0921c-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="0921c-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0921c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0921c-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0921c-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="0921c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0921c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0921c-141">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="0921c-141">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> <dt>

[<span data-ttu-id="0921c-142">**CountedString**</span><span class="sxs-lookup"><span data-stu-id="0921c-142">**CountedString**</span></span>](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





