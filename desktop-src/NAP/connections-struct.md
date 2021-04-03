---
title: Estructura de conexiones (NapEnforcementClient. h)
description: Contiene información sobre la lista de conexiones mantenida por un aplicador.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Estructura de conexiones NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997157"
---
# <a name="connections-structure"></a><span data-ttu-id="7fa0c-104">Estructura de conexiones</span><span class="sxs-lookup"><span data-stu-id="7fa0c-104">Connections structure</span></span>

> [!Note]  
> <span data-ttu-id="7fa0c-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="7fa0c-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7fa0c-106">La estructura de **conexiones** contiene información sobre la lista de conexiones mantenida por un aplicador.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-106">The **Connections** structure contains information about the list of connections maintained by an enforcer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa0c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fa0c-107">Syntax</span></span>


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a><span data-ttu-id="7fa0c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7fa0c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7fa0c-109">**count**</span><span class="sxs-lookup"><span data-stu-id="7fa0c-109">**count**</span></span>
</dt> <dd>

<span data-ttu-id="7fa0c-110">El número de conexiones activas que mantiene actualmente un aplicador en el intervalo de 0 (cero) a [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7fa0c-110">The number of active connections currently maintained by an enforcer within the range 0 (zero) to [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fa0c-111">**connections**</span><span class="sxs-lookup"><span data-stu-id="7fa0c-111">**connections**</span></span>
</dt> <dd>

<span data-ttu-id="7fa0c-112">Puntero COM a una lista de interfaces [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) que representan las conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-112">A COM pointer to a list of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interfaces that represent client connections.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fa0c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fa0c-113">Requirements</span></span>



| <span data-ttu-id="7fa0c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa0c-114">Requirement</span></span> | <span data-ttu-id="7fa0c-115">Value</span><span class="sxs-lookup"><span data-stu-id="7fa0c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa0c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fa0c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa0c-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7fa0c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7fa0c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fa0c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa0c-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7fa0c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7fa0c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fa0c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fa0c-121"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fa0c-121"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="7fa0c-122">IDL</span><span class="sxs-lookup"><span data-stu-id="7fa0c-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7fa0c-123"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7fa0c-123"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fa0c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fa0c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa0c-125">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="7fa0c-125">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="7fa0c-126">Estructuras de NAP</span><span class="sxs-lookup"><span data-stu-id="7fa0c-126">NAP Structures</span></span>](nap-structures.md)
</dt> <dt>

[<span data-ttu-id="7fa0c-127">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="7fa0c-127">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





