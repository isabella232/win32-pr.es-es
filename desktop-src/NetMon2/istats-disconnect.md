---
description: Desconecta el NPP de la red.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: IStas::D método Ulta (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652883"
---
# <a name="istatsdisconnect-method"></a><span data-ttu-id="71efb-103">IStas::D método Ulta</span><span class="sxs-lookup"><span data-stu-id="71efb-103">IStats::Disconnect method</span></span>

<span data-ttu-id="71efb-104">El método **Disconnect** desconecta el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="71efb-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="71efb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71efb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="71efb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71efb-106">Parameters</span></span>

<span data-ttu-id="71efb-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="71efb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71efb-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71efb-108">Return value</span></span>

<span data-ttu-id="71efb-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="71efb-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="71efb-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="71efb-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="71efb-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="71efb-111">Return code</span></span>                                                                                            | <span data-ttu-id="71efb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="71efb-112">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71efb-113"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71efb-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="71efb-114">NPP está capturando datos actualmente.</span><span class="sxs-lookup"><span data-stu-id="71efb-114">The NPP is currently capturing data.</span></span> <span data-ttu-id="71efb-115">No se puede desconectar de la red mientras haya una captura de datos en curso.</span><span class="sxs-lookup"><span data-stu-id="71efb-115">You cannot disconnect from the network while a data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="71efb-116"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="71efb-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="71efb-117">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="71efb-117">The NPP is not connected to the network.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="71efb-118"><dt>**NMERR \_ no \_ solo estadísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71efb-118"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="71efb-119">NPP está conectado a la red, pero no con el método [**istas:: Connect**](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="71efb-119">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="71efb-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71efb-120">Remarks</span></span>

<span data-ttu-id="71efb-121">No se puede llamar a este método cuando NPP está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="71efb-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="71efb-122">Llame primero al método **istas::D Ulta** y, a continuación, llame a los [**ISTA:: Stop**](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="71efb-122">Call the **IStats::Disconnect** method first and then call [**IStats::Stop**](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71efb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71efb-123">Requirements</span></span>



| <span data-ttu-id="71efb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="71efb-124">Requirement</span></span> | <span data-ttu-id="71efb-125">Value</span><span class="sxs-lookup"><span data-stu-id="71efb-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71efb-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71efb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="71efb-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="71efb-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="71efb-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71efb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="71efb-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71efb-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="71efb-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71efb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="71efb-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="71efb-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="71efb-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71efb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71efb-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71efb-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71efb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="71efb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71efb-135">**IStas**</span><span class="sxs-lookup"><span data-stu-id="71efb-135">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="71efb-136">**ISta:: Connect**</span><span class="sxs-lookup"><span data-stu-id="71efb-136">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="71efb-137">**IStas:: Stop**</span><span class="sxs-lookup"><span data-stu-id="71efb-137">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 




