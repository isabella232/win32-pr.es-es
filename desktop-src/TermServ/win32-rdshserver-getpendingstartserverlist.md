---
title: Método GetPendingStartServerList de la clase Win32_RDSHServer
description: Recupera una lista de servidores en espera de inicio.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Método GetPendingStartServerList Servicios de Escritorio remoto
- Método GetPendingStartServerList Servicios de Escritorio remoto, clase Win32_RDSHServer
- Win32_RDSHServer de clase Servicios de Escritorio remoto, método GetPendingStartServerList
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422362"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="06606-106">Método GetPendingStartServerList de la \_ clase RDSHServer de Win32</span><span class="sxs-lookup"><span data-stu-id="06606-106">GetPendingStartServerList method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="06606-107">Recupera una lista de servidores en espera de inicio.</span><span class="sxs-lookup"><span data-stu-id="06606-107">Retrieves a list of server waiting to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="06606-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06606-108">Syntax</span></span>


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a><span data-ttu-id="06606-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06606-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06606-110">*maxServers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06606-110">*maxServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06606-111">Número máximo de servidores que se van a devolver en la lista.</span><span class="sxs-lookup"><span data-stu-id="06606-111">The maximum number of servers to return in the list.</span></span>

</dd> <dt>

<span data-ttu-id="06606-112">*ServerFQDNs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="06606-112">*ServerFQDNs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06606-113">Si se ejecuta correctamente, contiene una colección de nombres de dominio completos de los servidores a la espera de iniciarse.</span><span class="sxs-lookup"><span data-stu-id="06606-113">On success, contains a collection of fully-qualified domain names of the servers waiting to start.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06606-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06606-114">Remarks</span></span>

<span data-ttu-id="06606-115">La lista de servidores se restablece después de cada llamada, de modo que la siguiente llamada no obtenga un servidor duplicado.</span><span class="sxs-lookup"><span data-stu-id="06606-115">The list of servers is reset after every call, so that the next call will not get a duplicate server.</span></span>

## <a name="requirements"></a><span data-ttu-id="06606-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06606-116">Requirements</span></span>



| <span data-ttu-id="06606-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="06606-117">Requirement</span></span> | <span data-ttu-id="06606-118">Value</span><span class="sxs-lookup"><span data-stu-id="06606-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="06606-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06606-119">Minimum supported client</span></span><br/> | <span data-ttu-id="06606-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="06606-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="06606-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06606-121">Minimum supported server</span></span><br/> | <span data-ttu-id="06606-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="06606-122">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="06606-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="06606-123">Namespace</span></span><br/>                | <span data-ttu-id="06606-124">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="06606-124">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="06606-125">MOF</span><span class="sxs-lookup"><span data-stu-id="06606-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06606-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06606-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="06606-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="06606-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06606-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06606-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="06606-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="06606-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06606-130">**Win32 \_ RDSHServer**</span><span class="sxs-lookup"><span data-stu-id="06606-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





