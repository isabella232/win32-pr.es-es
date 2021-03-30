---
description: El experto implementa la función DllMain. El sistema operativo llama a DllMain para obtener un identificador para una instancia del experto.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: Función de devolución de llamada del experto de DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910889"
---
# <a name="dllmain-expert-callback-function"></a><span data-ttu-id="81847-104">Función de devolución de llamada del experto DllMain</span><span class="sxs-lookup"><span data-stu-id="81847-104">DllMain Expert callback function</span></span>

<span data-ttu-id="81847-105">El experto implementa la función [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="81847-105">The expert implements the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> <span data-ttu-id="81847-106">El sistema operativo llama a **DllMain** para obtener un identificador para una instancia del experto.</span><span class="sxs-lookup"><span data-stu-id="81847-106">The operating system calls **DllMain** to obtain a handle to an instance of the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="81847-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81847-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="81847-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81847-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81847-109">*hInstance* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="81847-109">*hInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81847-110">Identificador de una instancia del experto.</span><span class="sxs-lookup"><span data-stu-id="81847-110">Handle to an instance of the expert.</span></span>

<span data-ttu-id="81847-111">Si el experto usa la interfaz de usuario Monitor de red, el valor de *hInstance* debe almacenarse en una variable global.</span><span class="sxs-lookup"><span data-stu-id="81847-111">If the expert uses the Network Monitor user interface, the *hInstance* value must be stored in a global variable.</span></span> <span data-ttu-id="81847-112">Este enfoque solo es necesario cuando el valor del parámetro *ulReason* se establece en dll \_ Process \_ Attach.</span><span class="sxs-lookup"><span data-stu-id="81847-112">This approach is necessary only when the value of the *ulReason* parameter is set to DLL\_PROCESS\_ATTACH.</span></span>

</dd> <dt>

<span data-ttu-id="81847-113">*ulReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81847-113">*ulReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81847-114">Indicador de por qué se llamó a la función.</span><span class="sxs-lookup"><span data-stu-id="81847-114">Indicator of why the function was called.</span></span> <span data-ttu-id="81847-115">Un valor de DLL \_ Process \_ Attach (que se aplica cuando se carga el archivo dll por primera vez) indica que el experto debe guardar el valor de *hInstance* en una variable global.</span><span class="sxs-lookup"><span data-stu-id="81847-115">A value of DLL\_PROCESS\_ATTACH, (which applies when the DLL is first loaded) indicates that the expert should save the *hInstance* value in a global variable.</span></span>

<span data-ttu-id="81847-116">Con cualquier otro valor, se pueden omitir todas las llamadas a la función [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="81847-116">With any other value, all calls to the [**DllMain**](/windows/desktop/Dlls/dllmain) function can be ignored.</span></span> <span data-ttu-id="81847-117">Para obtener una lista de todas las marcas posibles establecidas por el sistema operativo, vea **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="81847-117">For a list of all possible flags set by the operating system, see **DLLMain**.</span></span>

</dd> <dt>

<span data-ttu-id="81847-118">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="81847-118">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="81847-119">El parámetro no está en uso.</span><span class="sxs-lookup"><span data-stu-id="81847-119">Parameter is not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81847-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81847-120">Return value</span></span>

<span data-ttu-id="81847-121">Si la función se realiza correctamente, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="81847-121">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="81847-122">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="81847-122">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="81847-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81847-123">Remarks</span></span>

<span data-ttu-id="81847-124">El sistema operativo llama a la función experta de **DllMain** cuando un proceso carga o descarga el archivo dll de expertos.</span><span class="sxs-lookup"><span data-stu-id="81847-124">The operating system calls the **DllMain** expert function when a process loads or unloads the expert DLL.</span></span> <span data-ttu-id="81847-125">La función de experto de **DllMain** solo se debe exportar si el experto tiene una interfaz de usuario para ver la configuración o los resultados y, a continuación, solo para devolver el valor de *hInstance* adecuado.</span><span class="sxs-lookup"><span data-stu-id="81847-125">The **DllMain** expert function must be exported only if the expert has a user interface for viewing either configuration or results, and then only to return the proper *hInstance* value.</span></span>

<span data-ttu-id="81847-126">La función del experto de **DllMain** se basa en la función [**DllMain**](/windows/desktop/Dlls/dllmain) de la biblioteca de vínculos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="81847-126">The **DllMain** expert function is based on the dynamic link library [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="81847-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81847-127">Requirements</span></span>



| <span data-ttu-id="81847-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="81847-128">Requirement</span></span> | <span data-ttu-id="81847-129">Value</span><span class="sxs-lookup"><span data-stu-id="81847-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81847-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81847-130">Minimum supported client</span></span><br/> | <span data-ttu-id="81847-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="81847-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="81847-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81847-132">Minimum supported server</span></span><br/> | <span data-ttu-id="81847-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81847-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="81847-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81847-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="81847-135"><dt>Process. h</dt></span><span class="sxs-lookup"><span data-stu-id="81847-135"><dt>Process.h</dt></span></span> </dl> |



 

