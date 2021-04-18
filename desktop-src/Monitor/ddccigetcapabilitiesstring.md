---
title: DDCCIGetCapabilitiesString función)
description: Obtiene una cadena que describe las funciones de un monitor.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Configuración del monitor de función DDCCIGetCapabilitiesString
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665991"
---
# <a name="ddccigetcapabilitiesstring-function"></a><span data-ttu-id="c353d-104">DDCCIGetCapabilitiesString función)</span><span class="sxs-lookup"><span data-stu-id="c353d-104">DDCCIGetCapabilitiesString function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c353d-105">La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c353d-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="c353d-106">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="c353d-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="c353d-107">Obtiene una cadena que describe las funciones de un monitor.</span><span class="sxs-lookup"><span data-stu-id="c353d-107">Gets a string that describes the capabilities of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="c353d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c353d-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="c353d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c353d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c353d-110">*hMonitor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c353d-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c353d-111">Identificador de un monitor físico.</span><span class="sxs-lookup"><span data-stu-id="c353d-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="c353d-112">*pszString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c353d-112">*pszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c353d-113">Un puntero a un búfer que recibe la cadena de funciones.</span><span class="sxs-lookup"><span data-stu-id="c353d-113">A pointer to a buffer that receives the capabilities string.</span></span> <span data-ttu-id="c353d-114">Para obtener la longitud de la cadena de funcionalidades, llame a [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span><span class="sxs-lookup"><span data-stu-id="c353d-114">To get the length of the capabilities string, call [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span></span>

</dd> <dt>

<span data-ttu-id="c353d-115">*dwLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c353d-115">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c353d-116">Tamaño del búfer de *pszString* , en caracteres, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="c353d-116">The size of the *pszString* buffer, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c353d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c353d-117">Return value</span></span>

<span data-ttu-id="c353d-118">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c353d-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="c353d-119">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="c353d-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c353d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c353d-120">Remarks</span></span>

<span data-ttu-id="c353d-121">Las aplicaciones deben llamar a [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) en lugar de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="c353d-121">Applications should call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) instead of calling this function.</span></span>

<span data-ttu-id="c353d-122">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="c353d-122">This function has no associated import library.</span></span> <span data-ttu-id="c353d-123">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="c353d-123">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c353d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c353d-124">Requirements</span></span>



| <span data-ttu-id="c353d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c353d-125">Requirement</span></span> | <span data-ttu-id="c353d-126">Value</span><span class="sxs-lookup"><span data-stu-id="c353d-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c353d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c353d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c353d-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c353d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c353d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c353d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c353d-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c353d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c353d-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c353d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c353d-132"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c353d-132"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c353d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c353d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c353d-134">Supervisar funciones de configuración</span><span class="sxs-lookup"><span data-stu-id="c353d-134">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

