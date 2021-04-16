---
description: Busca un archivo en la memoria caché de Archivos sin conexión que cumpla los criterios especificados.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: CSCFindFirstFileW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: f8cad9caf78b44f40a4126307db6deb0f71dfd1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650010"
---
# <a name="cscfindfirstfilew-function"></a><span data-ttu-id="90a6d-103">CSCFindFirstFileW función)</span><span class="sxs-lookup"><span data-stu-id="90a6d-103">CSCFindFirstFileW function</span></span>

<span data-ttu-id="90a6d-104">\[Esta función no se admite y no debe usarse.\]</span><span class="sxs-lookup"><span data-stu-id="90a6d-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="90a6d-105">Busca un archivo en la memoria caché de Archivos sin conexión que cumpla los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="90a6d-105">Searches for a file in the Offline Files cache that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a6d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90a6d-106">Syntax</span></span>


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="90a6d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90a6d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90a6d-108">*lpszFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90a6d-108">*lpszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a6d-109">Puntero a una cadena terminada en null que especifica un directorio o ruta de acceso UNC válida.</span><span class="sxs-lookup"><span data-stu-id="90a6d-109">A pointer to a null-terminated string that specifies a valid UNC directory or path.</span></span>

</dd> <dt>

<span data-ttu-id="90a6d-110">*lpFind32* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90a6d-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90a6d-111">Puntero a la estructura [**de \_ \_ datos de búsqueda de Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) que recibe información sobre el archivo o subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="90a6d-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="90a6d-112">*lpdwStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90a6d-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90a6d-113">Código NTSTATUS que indica el estado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="90a6d-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="90a6d-114">*lpdwPinCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90a6d-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90a6d-115">Este parámetro es distinto de cero si el archivo está disponible sin conexión o 0 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="90a6d-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="90a6d-116">*lpdwHintFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90a6d-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90a6d-117">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="90a6d-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="90a6d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="90a6d-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="90a6d-119">Significado</span><span class="sxs-lookup"><span data-stu-id="90a6d-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="90a6d-120"><dt>**Marca \_ de \_Usuario de \_ PIN \_ de sugerencia de CSC**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="90a6d-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="90a6d-121">Un usuario ha hecho que el archivo esté disponible sin conexión.</span><span class="sxs-lookup"><span data-stu-id="90a6d-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="90a6d-122"><dt>**Marca \_ de El \_ PIN de sugerencia de CSC \_ hereda el \_ \_ usuario**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="90a6d-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="90a6d-123">Un usuario ha hecho que el elemento primario esté disponible sin conexión y marcado como primario para que sus elementos secundarios estén disponibles sin conexión.</span><span class="sxs-lookup"><span data-stu-id="90a6d-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="90a6d-124"><dt>**Marca \_ de El \_ PIN de sugerencia de CSC \_ hereda el \_ \_ sistema**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="90a6d-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="90a6d-125">Un administrador o una directiva de grupo ha hecho que el elemento primario esté disponible sin conexión y marcado como elemento primario para que sus elementos secundarios estén disponibles sin conexión.</span><span class="sxs-lookup"><span data-stu-id="90a6d-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="90a6d-126"><dt>**Marca \_ de CSC \_ Hint \_ PIN \_ System**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="90a6d-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="90a6d-127">Un administrador o una directiva de grupo ha hecho que el archivo esté disponible sin conexión.</span><span class="sxs-lookup"><span data-stu-id="90a6d-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="90a6d-128">*lpOrgFileTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90a6d-128">*lpOrgFileTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90a6d-129">Un puntero a una estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para recibir la información de fecha y hora para el archivo o subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="90a6d-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90a6d-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90a6d-130">Return value</span></span>

<span data-ttu-id="90a6d-131">Si la función se ejecuta correctamente, el valor devuelto es un identificador de búsqueda que se usa en una llamada subsiguiente a [**CSCFindNextFileW**](cscfindnextfilew.md) o [**CSCFindClose**](cscfindclose.md).</span><span class="sxs-lookup"><span data-stu-id="90a6d-131">If the function succeeds, the return value is a search handle used in a subsequent call to [**CSCFindNextFileW**](cscfindnextfilew.md) or [**CSCFindClose**](cscfindclose.md).</span></span>

<span data-ttu-id="90a6d-132">Si la función no se ejecuta correctamente, el valor devuelto es **INVALID\_HANDLE\_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="90a6d-132">If the function fails, the return value is **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="90a6d-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90a6d-133">Remarks</span></span>

<span data-ttu-id="90a6d-134">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="90a6d-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a6d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90a6d-135">Requirements</span></span>



| <span data-ttu-id="90a6d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="90a6d-136">Requirement</span></span> | <span data-ttu-id="90a6d-137">Value</span><span class="sxs-lookup"><span data-stu-id="90a6d-137">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90a6d-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="90a6d-138">DLL</span></span><br/> | <dl> <span data-ttu-id="90a6d-139"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90a6d-139"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
