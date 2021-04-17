---
description: Las constantes siguientes pueden devolverse como errores.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: Constantes de RND_ (Rnderr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690314"
---
# <a name="rnd_-constants"></a><span data-ttu-id="0cadb-103">RND ( \_ constantes)</span><span class="sxs-lookup"><span data-stu-id="0cadb-103">RND\_ Constants</span></span>

<span data-ttu-id="0cadb-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0cadb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0cadb-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0cadb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0cadb-106">Las constantes siguientes pueden devolverse como errores.</span><span class="sxs-lookup"><span data-stu-id="0cadb-106">The following constants may be returned as errors.</span></span>

<dl> <dt>

<span data-ttu-id="0cadb-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND \_ hora no válida \_**</span><span class="sxs-lookup"><span data-stu-id="0cadb-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="0cadb-108">0xe0000200</span><span class="sxs-lookup"><span data-stu-id="0cadb-108">0xe0000200</span></span>
</dt> <dt>



<span data-ttu-id="0cadb-109">El valor de hora especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="0cadb-109">The time value entered is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cadb-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND \_ \_ nombre de servidor null \_**</span><span class="sxs-lookup"><span data-stu-id="0cadb-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND\_NULL\_SERVER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="0cadb-111">0xe0000201</span><span class="sxs-lookup"><span data-stu-id="0cadb-111">0xe0000201</span></span>
</dt> <dt>



<span data-ttu-id="0cadb-112">El nombre del servidor es **null**, probablemente porque [**ITConferenceBlob:: init**](itconferenceblob-init.md) no se ha ejecutado o no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0cadb-112">The server name is **NULL**, probably because [**ITConferenceBlob::Init**](itconferenceblob-init.md) has not been run or did not succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cadb-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND \_ ya está \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="0cadb-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="0cadb-114">0xe0000202</span><span class="sxs-lookup"><span data-stu-id="0cadb-114">0xe0000202</span></span>
</dt> <dt>



<span data-ttu-id="0cadb-115">Se llamó al método [**ITDirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) , pero ya existe una conexión.</span><span class="sxs-lookup"><span data-stu-id="0cadb-115">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method was called, but a connection already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cadb-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ no \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="0cadb-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="0cadb-117">0xe0000203</span><span class="sxs-lookup"><span data-stu-id="0cadb-117">0xe0000203</span></span>
</dt> <dt>



<span data-ttu-id="0cadb-118">No se ha llamado al método [**ITDirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) o se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="0cadb-118">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method has not been called, or failed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0cadb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cadb-119">Requirements</span></span>



| <span data-ttu-id="0cadb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cadb-120">Requirement</span></span> | <span data-ttu-id="0cadb-121">Value</span><span class="sxs-lookup"><span data-stu-id="0cadb-121">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0cadb-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="0cadb-122">TAPI version</span></span><br/> | <span data-ttu-id="0cadb-123">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0cadb-123">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="0cadb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cadb-124">Header</span></span><br/>       | <dl> <span data-ttu-id="0cadb-125"><dt>Rnderr. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cadb-125"><dt>Rnderr.h</dt></span></span> </dl> |



 

 




