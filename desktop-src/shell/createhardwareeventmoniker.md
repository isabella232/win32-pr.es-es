---
description: Crea un moniker que representa un componente de hardware y su controlador de eventos asociado. AutoPlay usa esta función para permitir que las aplicaciones usen eventos de Reproducción automática.
title: Función CreateHardwareEventMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: c22f01835f9c526e95a4330e6ad35d370421e604
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841246"
---
# <a name="createhardwareeventmoniker-function"></a><span data-ttu-id="3d6cf-104">Función CreateHardwareEventMoniker</span><span class="sxs-lookup"><span data-stu-id="3d6cf-104">CreateHardwareEventMoniker function</span></span>

<span data-ttu-id="3d6cf-105">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="3d6cf-106">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3d6cf-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3d6cf-107">Crea un moniker que representa un componente de hardware y su controlador de eventos asociado.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-107">Creates a moniker representing a hardware component and its associated event handler.</span></span> <span data-ttu-id="3d6cf-108">AutoPlay usa esta función para permitir que las aplicaciones usen eventos de Reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-108">AutoPlay uses this function to allow applications to use AutoPlay events.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d6cf-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d6cf-109">Syntax</span></span>


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a><span data-ttu-id="3d6cf-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d6cf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d6cf-111">*clsid* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3d6cf-111">*clsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6cf-112">Tipo: **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="3d6cf-112">Type: **REFCLSID**</span></span>

<span data-ttu-id="3d6cf-113">Identificador de la clase a la que se enlaza el moniker.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-113">The ID of the class to which the moniker binds.</span></span>

</dd> <dt>

<span data-ttu-id="3d6cf-114">*pszEventHandler* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3d6cf-114">*pszEventHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6cf-115">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="3d6cf-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="3d6cf-116">Nombre del controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-116">The name of the event handler.</span></span>

</dd> <dt>

<span data-ttu-id="3d6cf-117">*ppmoniker* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d6cf-117">*ppmoniker* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d6cf-118">Tipo: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span><span class="sxs-lookup"><span data-stu-id="3d6cf-118">Type: **[**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span></span>

<span data-ttu-id="3d6cf-119">Dirección de una variable de puntero que recibe el [**puntero de interfaz IMoniker.**](/windows/win32/api/objidl/nn-objidl-imoniker)</span><span class="sxs-lookup"><span data-stu-id="3d6cf-119">The address of a pointer variable that receives the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d6cf-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d6cf-120">Return value</span></span>

<span data-ttu-id="3d6cf-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3d6cf-121">Type: **HRESULT**</span></span>

<span data-ttu-id="3d6cf-122">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3d6cf-123">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="3d6cf-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d6cf-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d6cf-124">Remarks</span></span>

<span data-ttu-id="3d6cf-125">Use **CreateHardwareEventMoniker al** registrar aplicaciones en ejecución para que esas aplicaciones tengan acceso a eventos de Reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-125">Use **CreateHardwareEventMoniker** when registering running applications so that those applications have access to AutoPlay events.</span></span> <span data-ttu-id="3d6cf-126">Para usar eventos de Reproducción automática en aplicaciones en ejecución, primero debe crear un nuevo componente que implemente la [**interfaz IHWEventHandler.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)</span><span class="sxs-lookup"><span data-stu-id="3d6cf-126">To use AutoPlay events in running applications, you must first create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span> <span data-ttu-id="3d6cf-127">Inicialice esta interfaz con el valor InitCmdLine de la entrada del controlador en particular en la clave **Handlers,** ya que AutoPlay no llama al [**método Initialize.**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize)</span><span class="sxs-lookup"><span data-stu-id="3d6cf-127">Initialize this interface with the InitCmdLine value from the particular handler's entry under the **Handlers** key, because AutoPlay does not call the [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method.</span></span>

<span data-ttu-id="3d6cf-128">Debe llamar a **CreateHardwareEventMoniker para** obtener un moniker que represente el componente y su controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-128">You should call **CreateHardwareEventMoniker** to get a moniker that represents your component and its event handler.</span></span> <span data-ttu-id="3d6cf-129">A continuación, use el valor devuelto en el *parámetro ppmoniker* para registrar el componente en la tabla de objetos en ejecución (ROT), como se muestra en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-129">Then, use the value returned in the *ppmoniker* parameter to register your component in the running object table (ROT) as shown in the example.</span></span>

<span data-ttu-id="3d6cf-130">Tenga en **cuenta que CreateHardwareEventMoniker** no está definido en un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-130">Note that **CreateHardwareEventMoniker** is not defined in a header file.</span></span> <span data-ttu-id="3d6cf-131">Para usarlo en el código, debe obtener un identificador para el archivo Shsvcs.dll a través de una llamada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="3d6cf-131">To use it in your code, you must obtain a handle to the Shsvcs.dll file through a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span> <span data-ttu-id="3d6cf-132">A continuación, use ese identificador en una llamada a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obtener una instancia de la **función CreateHardwareEventMoniker.**</span><span class="sxs-lookup"><span data-stu-id="3d6cf-132">You then use that handle in a call to [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain an instance of the **CreateHardwareEventMoniker** function.</span></span>

<span data-ttu-id="3d6cf-133">La llamada a [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requiere que escriba la siguiente **información de AppID** en el Registro.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-133">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that you enter the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a><span data-ttu-id="3d6cf-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d6cf-134">Requirements</span></span>



| <span data-ttu-id="3d6cf-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d6cf-135">Requirement</span></span> | <span data-ttu-id="3d6cf-136">Value</span><span class="sxs-lookup"><span data-stu-id="3d6cf-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6cf-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d6cf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3d6cf-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3d6cf-138">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3d6cf-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d6cf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3d6cf-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d6cf-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d6cf-141">Header</span><span class="sxs-lookup"><span data-stu-id="3d6cf-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d6cf-142"><dt>Ninguno</dt></span><span class="sxs-lookup"><span data-stu-id="3d6cf-142"><dt>None</dt></span></span> </dl>       |
| <span data-ttu-id="3d6cf-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d6cf-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d6cf-144"><dt>Shsvcs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d6cf-144"><dt>Shsvcs.dll</dt></span></span> </dl> |



 

 
