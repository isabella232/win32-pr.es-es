---
description: 'Método IRTC::D isconnect: el método Disconnect desconecta el NPP de la red.'
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: Método IRTC::D isconnect (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 43acb88e2c7b6108a162c4715de02375121021f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110723"
---
# <a name="irtcdisconnect-method"></a><span data-ttu-id="8b82c-103">Método IRTC::D isconnect</span><span class="sxs-lookup"><span data-stu-id="8b82c-103">IRTC::Disconnect method</span></span>

<span data-ttu-id="8b82c-104">El **método Disconnect** desconecta el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="8b82c-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b82c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b82c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="8b82c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b82c-106">Parameters</span></span>

<span data-ttu-id="8b82c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8b82c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b82c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b82c-108">Return value</span></span>

<span data-ttu-id="8b82c-109">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="8b82c-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8b82c-110">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="8b82c-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="8b82c-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8b82c-111">Return code</span></span>                                                                                          | <span data-ttu-id="8b82c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b82c-112">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b82c-113"><dt>**CAPTURA DE \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="8b82c-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="8b82c-114">El NPP captura datos.</span><span class="sxs-lookup"><span data-stu-id="8b82c-114">The NPP is capturing data.</span></span> <span data-ttu-id="8b82c-115">No se puede desconectar de la red mientras la captura de datos está en curso.</span><span class="sxs-lookup"><span data-stu-id="8b82c-115">You cannot disconnect from the network while the data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="8b82c-116"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="8b82c-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8b82c-117">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="8b82c-117">The NPP is not connected to the network.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="8b82c-118"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="8b82c-118"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="8b82c-119">El NPP está conectado a la red, pero no con el [método IRTC::Connect.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="8b82c-119">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="8b82c-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b82c-120">Remarks</span></span>

<span data-ttu-id="8b82c-121">No se puede llamar a este método cuando el NPP captura datos.</span><span class="sxs-lookup"><span data-stu-id="8b82c-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="8b82c-122">Debe llamar al método [IRTC::Stop](irtc-stop.md) antes de llamar a IRTC::D isconnect.</span><span class="sxs-lookup"><span data-stu-id="8b82c-122">You must call the [IRTC::Stop](irtc-stop.md) method before calling IRTC::Disconnect.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b82c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b82c-123">Requirements</span></span>



| <span data-ttu-id="8b82c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b82c-124">Requirement</span></span> | <span data-ttu-id="8b82c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8b82c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b82c-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b82c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8b82c-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8b82c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="8b82c-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b82c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8b82c-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b82c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="8b82c-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b82c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b82c-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="8b82c-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="8b82c-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b82c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b82c-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b82c-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b82c-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8b82c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b82c-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="8b82c-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="8b82c-136">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="8b82c-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="8b82c-137">IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="8b82c-137">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




