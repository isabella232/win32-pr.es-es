---
description: Continúa una operación de búsqueda de archivos.
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: CSCFindNextFileW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindNextFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 50b387a1ff99a95fcbe0fae8fe8ad93d14c335b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660703"
---
# <a name="cscfindnextfilew-function"></a><span data-ttu-id="3062a-103">CSCFindNextFileW función)</span><span class="sxs-lookup"><span data-stu-id="3062a-103">CSCFindNextFileW function</span></span>

<span data-ttu-id="3062a-104">\[Esta función no se admite y no debe usarse.\]</span><span class="sxs-lookup"><span data-stu-id="3062a-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="3062a-105">Continúa una operación de búsqueda de archivos.</span><span class="sxs-lookup"><span data-stu-id="3062a-105">Continues a file search operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3062a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3062a-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindNextFileW(
  _In_  HANDLE           hFind,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _In_  FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="3062a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3062a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3062a-108">*hFind* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3062a-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3062a-109">Identificador de búsqueda devuelto por la función [**CSCFindFirstFileW**](cscfindfirstfilew.md) .</span><span class="sxs-lookup"><span data-stu-id="3062a-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3062a-110">*lpFind32* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3062a-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3062a-111">Puntero a la estructura [**de \_ \_ datos de búsqueda de Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) que recibe información sobre el archivo o subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="3062a-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="3062a-112">*lpdwStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3062a-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3062a-113">Código NTSTATUS que indica el estado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3062a-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="3062a-114">*lpdwPinCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3062a-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3062a-115">Este parámetro es distinto de cero si el archivo está disponible sin conexión o 0 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3062a-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="3062a-116">*lpdwHintFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3062a-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3062a-117">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3062a-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3062a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3062a-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="3062a-119">Significado</span><span class="sxs-lookup"><span data-stu-id="3062a-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="3062a-120"><dt>**Marca \_ de \_Usuario de \_ PIN \_ de sugerencia de CSC**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="3062a-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="3062a-121">Un usuario ha hecho que el archivo esté disponible sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3062a-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="3062a-122"><dt>**Marca \_ de El \_ PIN de sugerencia de CSC \_ hereda el \_ \_ usuario**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="3062a-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="3062a-123">Un usuario ha hecho que el elemento primario esté disponible sin conexión y marcado como primario para que sus elementos secundarios estén disponibles sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3062a-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="3062a-124"><dt>**Marca \_ de El \_ PIN de sugerencia de CSC \_ hereda el \_ \_ sistema**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="3062a-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="3062a-125">Un administrador o una directiva de grupo ha hecho que el elemento primario esté disponible sin conexión y marcado como elemento primario para que sus elementos secundarios estén disponibles sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3062a-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="3062a-126"><dt>**Marca \_ de CSC \_ Hint \_ PIN \_ System**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="3062a-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="3062a-127">Un administrador o una directiva de grupo ha hecho que el archivo esté disponible sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3062a-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="3062a-128">*lpOrgFileTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3062a-128">*lpOrgFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3062a-129">Un puntero a una estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para recibir la información de fecha y hora para el archivo o subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="3062a-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3062a-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3062a-130">Return value</span></span>

<span data-ttu-id="3062a-131">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="3062a-131">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3062a-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3062a-132">Remarks</span></span>

<span data-ttu-id="3062a-133">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3062a-133">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3062a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3062a-134">Requirements</span></span>



| <span data-ttu-id="3062a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3062a-135">Requirement</span></span> | <span data-ttu-id="3062a-136">Value</span><span class="sxs-lookup"><span data-stu-id="3062a-136">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3062a-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3062a-137">DLL</span></span><br/> | <dl> <span data-ttu-id="3062a-138"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3062a-138"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
