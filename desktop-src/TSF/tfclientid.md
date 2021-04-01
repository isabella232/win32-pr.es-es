---
title: TfClientId (msctf. h)
description: El tipo de datos TfClientId se usa para identificar al cliente.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801807"
---
# <a name="tfclientid"></a><span data-ttu-id="91fd3-104">TfClientId</span><span class="sxs-lookup"><span data-stu-id="91fd3-104">TfClientId</span></span>

<span data-ttu-id="91fd3-105">El tipo de datos **TfClientId** se usa para identificar al cliente.</span><span class="sxs-lookup"><span data-stu-id="91fd3-105">The **TfClientId** data type is used to identify the client.</span></span>


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a><span data-ttu-id="91fd3-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91fd3-106">Remarks</span></span>

<span data-ttu-id="91fd3-107">En TSF, las aplicaciones y los servicios de texto se conocen generalmente como clientes.</span><span class="sxs-lookup"><span data-stu-id="91fd3-107">Within TSF, applications and text services are generally referred to as clients.</span></span> <span data-ttu-id="91fd3-108">Cada cliente recibe un identificador único que usa para identificarse cuando se llama a varios métodos del administrador de TSF.</span><span class="sxs-lookup"><span data-stu-id="91fd3-108">Each client receives a unique identifier that it uses to identify itself when calling various TSF manager methods.</span></span> <span data-ttu-id="91fd3-109">Este identificador es del tipo **TfClientId** .</span><span class="sxs-lookup"><span data-stu-id="91fd3-109">This identifier is of the **TfClientId** type.</span></span>

<span data-ttu-id="91fd3-110">El tipo de datos **TfClientId** es proporcionado por el administrador de TSF.</span><span class="sxs-lookup"><span data-stu-id="91fd3-110">The **TfClientId** data type is supplied by the TSF manager.</span></span> <span data-ttu-id="91fd3-111">Una aplicación obtiene un valor **TfClientId** cuando llama a [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span><span class="sxs-lookup"><span data-stu-id="91fd3-111">An application obtains a **TfClientId** value when it calls [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span> <span data-ttu-id="91fd3-112">El valor TfClientId de un servicio de texto se pasa al método [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) .</span><span class="sxs-lookup"><span data-stu-id="91fd3-112">The TfClientId value for a text service is passed to the [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span> <span data-ttu-id="91fd3-113">Cualquier objeto que no se ajuste a las categorías anteriores puede obtener un identificador de cliente mediante una llamada a [ITfClientId:: GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span><span class="sxs-lookup"><span data-stu-id="91fd3-113">Any object that does not fit the above categories can obtain a client identifier by calling [ITfClientId::GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span></span>

## <a name="requirements"></a><span data-ttu-id="91fd3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91fd3-114">Requirements</span></span>



| <span data-ttu-id="91fd3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="91fd3-115">Requirement</span></span> | <span data-ttu-id="91fd3-116">Value</span><span class="sxs-lookup"><span data-stu-id="91fd3-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="91fd3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91fd3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91fd3-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="91fd3-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="91fd3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91fd3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91fd3-120">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="91fd3-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="91fd3-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="91fd3-121">Redistributable</span></span><br/>          | <span data-ttu-id="91fd3-122">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="91fd3-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="91fd3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91fd3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="91fd3-124"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="91fd3-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="91fd3-125">IDL</span><span class="sxs-lookup"><span data-stu-id="91fd3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="91fd3-126"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="91fd3-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91fd3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="91fd3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91fd3-128">**ITfClientId::GetClientId**</span><span class="sxs-lookup"><span data-stu-id="91fd3-128">**ITfClientId::GetClientId**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[<span data-ttu-id="91fd3-129">**ITfTextInputProcessor:: Activate**</span><span class="sxs-lookup"><span data-stu-id="91fd3-129">**ITfTextInputProcessor::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="91fd3-130">**ITfThreadMgr:: Activate**</span><span class="sxs-lookup"><span data-stu-id="91fd3-130">**ITfThreadMgr::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





