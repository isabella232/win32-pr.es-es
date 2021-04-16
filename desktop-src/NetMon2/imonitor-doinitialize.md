---
description: El monitor debe implementar el método de la función de inicialización. MCSVC llama a este método para obtener un filtro de captura inmediatamente antes de llamar al método IRTCConnect de NPPs.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Método IMonitorDoInitialize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540179"
---
# <a name="imonitordoinitialize-method"></a><span data-ttu-id="18bb4-104">IMonitor::D método oInitialize</span><span class="sxs-lookup"><span data-stu-id="18bb4-104">IMonitor::DoInitialize method</span></span>

<span data-ttu-id="18bb4-105">El monitor debe implementar el método de la función de **inicialización** .</span><span class="sxs-lookup"><span data-stu-id="18bb4-105">The **DoInitialize** method must be implemented by the monitor.</span></span> <span data-ttu-id="18bb4-106">MCSVC llama a este método para obtener un filtro de captura inmediatamente antes de llamar al método [IRTC:: Connect](irtc-connect.md) de NPP.</span><span class="sxs-lookup"><span data-stu-id="18bb4-106">The MCSVC calls this method to obtain a capture filter immediately before calling the NPP's [IRTC::Connect](irtc-connect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18bb4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18bb4-107">Syntax</span></span>


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a><span data-ttu-id="18bb4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18bb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18bb4-109">*pUnkMonitorCtrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18bb4-109">*pUnkMonitorCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18bb4-110">Un puntero [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pasado por MCSVC.</span><span class="sxs-lookup"><span data-stu-id="18bb4-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer passed in by the MCSVC.</span></span> <span data-ttu-id="18bb4-111">Para obtener una interfaz de control de supervisión compatible, el monitor debe llamar a [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero.</span><span class="sxs-lookup"><span data-stu-id="18bb4-111">To obtain a supported monitor control interface, the monitor must call [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer.</span></span>

</dd> <dt>

<span data-ttu-id="18bb4-112">*hNPPBlob* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="18bb4-112">*hNPPBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18bb4-113">En la entrada, identificador de un BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="18bb4-113">On input, a handle to an NPP BLOB.</span></span>

<span data-ttu-id="18bb4-114">En la salida, un BLOB NPP que contiene un filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="18bb4-114">On output, an NPP BLOB that contains a capture filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18bb4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18bb4-115">Return value</span></span>

<span data-ttu-id="18bb4-116">Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError).</span><span class="sxs-lookup"><span data-stu-id="18bb4-116">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="18bb4-117">Si el método no se realiza correctamente, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="18bb4-117">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="18bb4-118">Si se genera un error, MCSVC no creará el monitor o llamará a [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="18bb4-118">On error, the MCSVC will not create the monitor or call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="18bb4-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18bb4-119">Remarks</span></span>

<span data-ttu-id="18bb4-120">MCSVC llama al método **CoInitialize** para realizar cualquier inicialización del monitor necesaria.</span><span class="sxs-lookup"><span data-stu-id="18bb4-120">The MCSVC calls the **DoInitialize** method to perform any required monitor initialization.</span></span>

## <a name="requirements"></a><span data-ttu-id="18bb4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18bb4-121">Requirements</span></span>



| <span data-ttu-id="18bb4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="18bb4-122">Requirement</span></span> | <span data-ttu-id="18bb4-123">Value</span><span class="sxs-lookup"><span data-stu-id="18bb4-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="18bb4-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18bb4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="18bb4-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="18bb4-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="18bb4-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18bb4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="18bb4-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18bb4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="18bb4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18bb4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="18bb4-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="18bb4-129"><dt>Netmon.h</dt></span></span> </dl> |



 

