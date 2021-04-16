---
title: Enumeración ConnectionStatus
description: Representa el estado del dispositivo en la red que se ha detectado por última vez.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- Enumeración de ConnectionStatus de media streaming API
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718769"
---
# <a name="connectionstatus-enumeration"></a><span data-ttu-id="2730d-104">Enumeración ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="2730d-104">ConnectionStatus enumeration</span></span>

<span data-ttu-id="2730d-105">Representa el estado del dispositivo en la red que se ha detectado por última vez.</span><span class="sxs-lookup"><span data-stu-id="2730d-105">Represents the state of the device in the network as last seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="2730d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2730d-106">Syntax</span></span>


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a><span data-ttu-id="2730d-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="2730d-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2730d-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Pantalla**</span><span class="sxs-lookup"><span data-stu-id="2730d-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Online**</span></span>
</dt> <dd>

<span data-ttu-id="2730d-109">El dispositivo está en línea y activo en la red.</span><span class="sxs-lookup"><span data-stu-id="2730d-109">Device is online and active on the network.</span></span>

</dd> <dt>

<span data-ttu-id="2730d-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**N**</span><span class="sxs-lookup"><span data-stu-id="2730d-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**</span></span>
</dt> <dd>

<span data-ttu-id="2730d-111">El dispositivo está desconectado.</span><span class="sxs-lookup"><span data-stu-id="2730d-111">Device is offline.</span></span>

</dd> <dt>

<span data-ttu-id="2730d-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Actividad**</span><span class="sxs-lookup"><span data-stu-id="2730d-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Sleeping**</span></span>
</dt> <dd>

<span data-ttu-id="2730d-113">El dispositivo está actualmente sin conexión, pero se puede reactivar automáticamente cuando se realiza un intento de comunicación con él.</span><span class="sxs-lookup"><span data-stu-id="2730d-113">Device is currently offline but might automatically wake up when an attempt is made to communicate with it.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2730d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2730d-114">Requirements</span></span>



| <span data-ttu-id="2730d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2730d-115">Requirement</span></span> | <span data-ttu-id="2730d-116">Value</span><span class="sxs-lookup"><span data-stu-id="2730d-116">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2730d-117">IDL</span><span class="sxs-lookup"><span data-stu-id="2730d-117">IDL</span></span><br/> | <dl> <span data-ttu-id="2730d-118"><dt>Windows. Media. streaming. idl (referencia a Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="2730d-118"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





