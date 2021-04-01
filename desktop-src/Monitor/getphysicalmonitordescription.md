---
title: GetPhysicalMonitorDescription función)
description: Obtiene una descripción de un monitor físico.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- Configuración del monitor de función GetPhysicalMonitorDescription
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259ced1185e229fccd426adfbf94fa47af22b170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150253"
---
# <a name="getphysicalmonitordescription-function"></a><span data-ttu-id="a591a-104">GetPhysicalMonitorDescription función)</span><span class="sxs-lookup"><span data-stu-id="a591a-104">GetPhysicalMonitorDescription function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a591a-105">La API de configuración de monitor usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="a591a-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="a591a-106">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="a591a-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="a591a-107">Obtiene una descripción de un monitor físico.</span><span class="sxs-lookup"><span data-stu-id="a591a-107">Gets a description of a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="a591a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a591a-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="a591a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a591a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a591a-110">*hMonitor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a591a-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a591a-111">Identificador de un monitor físico.</span><span class="sxs-lookup"><span data-stu-id="a591a-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="a591a-112">*dwPhysicalMonitorDescriptionSizeInChars* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a591a-112">*dwPhysicalMonitorDescriptionSizeInChars* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a591a-113">Número de caracteres de la matriz *szPhysicalMonitorDescription* .</span><span class="sxs-lookup"><span data-stu-id="a591a-113">The number of characters in the *szPhysicalMonitorDescription* array.</span></span>

</dd> <dt>

<span data-ttu-id="a591a-114">*szPhysicalMonitorDescription* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a591a-114">*szPhysicalMonitorDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a591a-115">Puntero a una matriz que recibe la descripción.</span><span class="sxs-lookup"><span data-stu-id="a591a-115">A pointer to an array that receives the description.</span></span> <span data-ttu-id="a591a-116">El número de elementos de la matriz debe ser al menos el tamaño de la **\_ Descripción del monitor \_ \_ físico**.</span><span class="sxs-lookup"><span data-stu-id="a591a-116">The number of elements in the array should be at least **PHYSICAL\_MONITOR\_DESCRIPTION\_SIZE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a591a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a591a-117">Return value</span></span>

<span data-ttu-id="a591a-118">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a591a-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="a591a-119">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="a591a-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a591a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a591a-120">Remarks</span></span>

<span data-ttu-id="a591a-121">En lugar de usar esta función, las aplicaciones deben llamar a una de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="a591a-121">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="a591a-122">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="a591a-122">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="a591a-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="a591a-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="a591a-124">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="a591a-124">This function has no associated import library.</span></span> <span data-ttu-id="a591a-125">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="a591a-125">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="a591a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a591a-126">Requirements</span></span>



| <span data-ttu-id="a591a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a591a-127">Requirement</span></span> | <span data-ttu-id="a591a-128">Value</span><span class="sxs-lookup"><span data-stu-id="a591a-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a591a-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a591a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a591a-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a591a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a591a-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a591a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a591a-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a591a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a591a-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a591a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a591a-134"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a591a-134"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a591a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a591a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a591a-136">Supervisar funciones de configuración</span><span class="sxs-lookup"><span data-stu-id="a591a-136">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

