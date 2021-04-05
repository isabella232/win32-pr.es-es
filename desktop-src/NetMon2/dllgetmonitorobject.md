---
description: La función DllGetMonitorObject debe ser implementada por el monitor. MCSVC llama a esta función para crear una instancia del monitor.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Función de devolución de llamada DllGetMonitorObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912841"
---
# <a name="dllgetmonitorobject-callback-function"></a><span data-ttu-id="33cfa-104">Función de devolución de llamada DllGetMonitorObject</span><span class="sxs-lookup"><span data-stu-id="33cfa-104">DllGetMonitorObject callback function</span></span>

<span data-ttu-id="33cfa-105">La función **DllGetMonitorObject** debe ser implementada por el monitor.</span><span class="sxs-lookup"><span data-stu-id="33cfa-105">The **DllGetMonitorObject** function must be implemented by the monitor.</span></span> <span data-ttu-id="33cfa-106">MCSVC llama a esta función para crear una instancia del monitor.</span><span class="sxs-lookup"><span data-stu-id="33cfa-106">The MCSVC calls this function to create an instance of the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="33cfa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33cfa-107">Syntax</span></span>


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="33cfa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33cfa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33cfa-109">*riid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33cfa-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33cfa-110">UUID de monitores, que se muestra a continuación, tal como se define en el archivo de encabezado IMonitor. h.</span><span class="sxs-lookup"><span data-stu-id="33cfa-110">UUID of monitors, shown below, as defined in the IMonitor.h header file.</span></span> <span data-ttu-id="33cfa-111">Si se proporciona un UUID no válido, se produce un error en la función y el monitor debe devolver E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="33cfa-111">If an invalid UUID is provided, the function fails, and the monitor must return E\_NOINTERFACE.</span></span>

``` syntax
IID_IMonitor
```

</dd> <dt>

<span data-ttu-id="33cfa-112">*ppObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="33cfa-112">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33cfa-113">Puntero a un puntero que recibe la interfaz solicitada en *riid*.</span><span class="sxs-lookup"><span data-stu-id="33cfa-113">Pointer to a pointer that receives the interface requested in *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33cfa-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33cfa-114">Return value</span></span>

<span data-ttu-id="33cfa-115">Si la función se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError).</span><span class="sxs-lookup"><span data-stu-id="33cfa-115">If the function is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="33cfa-116">Si la función no es correcta, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="33cfa-116">If the function is unsuccessful, the return value is a failure code.</span></span> <span data-ttu-id="33cfa-117">Cuando se devuelve un código de error, MCSVC no crea el objeto de supervisión y no se llama al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="33cfa-117">When a failure code is returned, the MCSVC does not create the monitor object, and the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method is not called on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="33cfa-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33cfa-118">Remarks</span></span>

<span data-ttu-id="33cfa-119">Se llama a la función **DllGetMonitorObject** cada vez que MCSVC intenta crear una instancia del monitor.</span><span class="sxs-lookup"><span data-stu-id="33cfa-119">The **DllGetMonitorObject** function is called each time the MCSVC tries to create an instance of the monitor.</span></span> <span data-ttu-id="33cfa-120">Esta función tiene un gran similitud con la función [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) más común.</span><span class="sxs-lookup"><span data-stu-id="33cfa-120">This function intentionally bears a strong resemblance to the more common [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) function.</span></span> <span data-ttu-id="33cfa-121">La principal diferencia es que un CLSID no se pasa a **DllGetMonitorObject**.</span><span class="sxs-lookup"><span data-stu-id="33cfa-121">The main difference is that a CLSID is not passed in to **DllGetMonitorObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="33cfa-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33cfa-122">Requirements</span></span>



| <span data-ttu-id="33cfa-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="33cfa-123">Requirement</span></span> | <span data-ttu-id="33cfa-124">Value</span><span class="sxs-lookup"><span data-stu-id="33cfa-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="33cfa-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33cfa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="33cfa-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="33cfa-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="33cfa-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33cfa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="33cfa-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="33cfa-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="33cfa-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33cfa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="33cfa-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="33cfa-130"><dt>Netmon.h</dt></span></span> </dl> |



 

