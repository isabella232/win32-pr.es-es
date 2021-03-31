---
title: GetProcessHandleFromHwnd función)
description: Recupera un identificador de proceso de un identificador de ventana.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Función GetProcessHandleFromHwnd accesibilidad de Windows
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150332"
---
# <a name="getprocesshandlefromhwnd-function"></a><span data-ttu-id="755c5-104">GetProcessHandleFromHwnd función)</span><span class="sxs-lookup"><span data-stu-id="755c5-104">GetProcessHandleFromHwnd function</span></span>

<span data-ttu-id="755c5-105">Recupera un identificador de proceso de un identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="755c5-105">Retrieves a process handle from a window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="755c5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="755c5-106">Syntax</span></span>


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="755c5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="755c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="755c5-108">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="755c5-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="755c5-109">Tipo: **[ **hWnd**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="755c5-109">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="755c5-110">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="755c5-110">The window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="755c5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="755c5-111">Return value</span></span>

<span data-ttu-id="755c5-112">Tipo: **[ **Handle**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="755c5-112">Type: **[**HANDLE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="755c5-113">Si es correcto, devuelve el identificador del proceso que posee la ventana.</span><span class="sxs-lookup"><span data-stu-id="755c5-113">If successful, returns the handle of the process that owns the window.</span></span>

<span data-ttu-id="755c5-114">Si no se realiza correctamente, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="755c5-114">If not successful, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="755c5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="755c5-115">Remarks</span></span>

<span data-ttu-id="755c5-116">En versiones anteriores del sistema operativo, un proceso podía abrir otro proceso (para tener acceso a su memoria, por ejemplo) usando [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span><span class="sxs-lookup"><span data-stu-id="755c5-116">In previous versions of the operating system, a process could open another process (to access its memory, for example) using [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span></span> <span data-ttu-id="755c5-117">Esta función se ejecuta correctamente si el autor de la llamada tiene los privilegios adecuados; Normalmente, el llamador y el proceso de destino deben ser el mismo usuario.</span><span class="sxs-lookup"><span data-stu-id="755c5-117">This function succeeds if the caller has appropriate privileges; usually the caller and target process must be the same user.</span></span>

<span data-ttu-id="755c5-118">En Windows Vista, sin embargo, se produce un error de [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) en el escenario en el que el llamador tiene UIAccess y el proceso de destino se eleva.</span><span class="sxs-lookup"><span data-stu-id="755c5-118">On Windows Vista, however, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) fails in the scenario where the caller has UIAccess, and the target process is elevated.</span></span> <span data-ttu-id="755c5-119">En este caso, el propietario del proceso de destino se encuentra en el grupo administradores, pero el proceso de llamada se ejecuta con el token restringido, por lo que no es miembro de este grupo y se le deniega el acceso al proceso elevado.</span><span class="sxs-lookup"><span data-stu-id="755c5-119">In this case, the owner of the target process is in the Administrators group, but the calling process is running with the restricted token, so does not have membership in this group, and is denied access to the elevated process.</span></span> <span data-ttu-id="755c5-120">Sin embargo, si el autor de la llamada tiene UIAccess, puede usar un enlace de Windows para insertar código en el proceso de destino y, desde dentro del proceso de destino, devolver un identificador al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="755c5-120">If the caller has UIAccess, however, they can use a windows hook to inject code into the target process, and from within the target process, send a handle back to the caller.</span></span>

<span data-ttu-id="755c5-121">**GetProcessHandleFromHwnd** es una función útil que utiliza esta técnica para obtener el identificador del proceso que posee el HWND especificado.</span><span class="sxs-lookup"><span data-stu-id="755c5-121">**GetProcessHandleFromHwnd** is a convenience function that uses this technique to obtain the handle of the process that owns the specified HWND.</span></span> <span data-ttu-id="755c5-122">Tenga en cuenta que solo se realiza correctamente en los casos en los que el llamador y el proceso de destino se ejecutan como el mismo usuario.</span><span class="sxs-lookup"><span data-stu-id="755c5-122">Note that it only succeeds in cases where the caller and target process are running as the same user.</span></span> <span data-ttu-id="755c5-123">El identificador devuelto tiene los siguientes privilegios: procesar identificador de proceso de máquina virtual proceso de operación de VM lectura de máquina virtual \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ escritura \| sincronizar.</span><span class="sxs-lookup"><span data-stu-id="755c5-123">The returned handle has the following privileges: PROCESS\_DUP\_HANDLE \| PROCESS\_VM\_OPERATION \| PROCESS\_VM\_READ \| PROCESS\_VM\_WRITE \| SYNCHRONIZE.</span></span> <span data-ttu-id="755c5-124">Si se requieren otros privilegios, es posible que sea necesario implementar la técnica de enlace explícitamente en lugar de utilizar esta función.</span><span class="sxs-lookup"><span data-stu-id="755c5-124">If other privileges are required, it may be necessary to implement the hooking technique explicitly instead of using this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="755c5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="755c5-125">Requirements</span></span>



| <span data-ttu-id="755c5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="755c5-126">Requirement</span></span> | <span data-ttu-id="755c5-127">Value</span><span class="sxs-lookup"><span data-stu-id="755c5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="755c5-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="755c5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="755c5-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="755c5-129">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="755c5-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="755c5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="755c5-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="755c5-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="755c5-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="755c5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="755c5-133"><dt>Oleacc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="755c5-133"><dt>Oleacc.dll</dt></span></span> </dl> |



 

