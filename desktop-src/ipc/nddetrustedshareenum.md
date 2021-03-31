---
description: Recupera los nombres de todos los recursos compartidos DDE de red que son de confianza en el contexto del proceso de llamada.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: Función NDdeTrustedShareEnum (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361248"
---
# <a name="nddetrustedshareenum-function"></a><span data-ttu-id="498a4-103">NDdeTrustedShareEnum función)</span><span class="sxs-lookup"><span data-stu-id="498a4-103">NDdeTrustedShareEnum function</span></span>

<span data-ttu-id="498a4-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="498a4-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="498a4-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="498a4-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="498a4-106">Recupera los nombres de todos los recursos compartidos DDE de red que son de confianza en el contexto del proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="498a4-106">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>

## <a name="syntax"></a><span data-ttu-id="498a4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="498a4-107">Syntax</span></span>


```C++
UINT NDdeTrustedShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="498a4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="498a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="498a4-109">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="498a4-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="498a4-110">Nombre del servidor en el que reside el DSDM.</span><span class="sxs-lookup"><span data-stu-id="498a4-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="498a4-111">*nLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="498a4-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="498a4-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="498a4-112">Reserved.</span></span> <span data-ttu-id="498a4-113">Este parámetro debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="498a4-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="498a4-114">*lpBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="498a4-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="498a4-115">Un puntero a un búfer que recibe la lista de recursos compartidos DDE de confianza.</span><span class="sxs-lookup"><span data-stu-id="498a4-115">A pointer to a buffer that receives the list of trusted DDE shares.</span></span> <span data-ttu-id="498a4-116">La lista de recursos compartidos DDE de confianza se devuelve como una secuencia de cadenas separadas por null que finalizan con un carácter nulo doble al final.</span><span class="sxs-lookup"><span data-stu-id="498a4-116">The list of trusted DDE shares is returned as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="498a4-117">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="498a4-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="498a4-118">Si el valor de *lpBuffer* es **null**, el DSDM devuelve el tamaño del búfer necesario para contener la lista de recursos compartidos en el campo *lpcbTotalAvailable* .</span><span class="sxs-lookup"><span data-stu-id="498a4-118">If the *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* field.</span></span>

</dd> <dt>

<span data-ttu-id="498a4-119">*cBufSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="498a4-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="498a4-120">Tamaño del búfer de *lpBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="498a4-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="498a4-121">Este parámetro debe ser cero si *lpBuffer* es **null**.</span><span class="sxs-lookup"><span data-stu-id="498a4-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="498a4-122">*lpnEntriesRead* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="498a4-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="498a4-123">Puntero a una variable que recibe el número total de recursos compartidos de confianza que se enumeran.</span><span class="sxs-lookup"><span data-stu-id="498a4-123">A pointer to a variable that receives the total number of trusted shares being enumerated.</span></span> <span data-ttu-id="498a4-124">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="498a4-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="498a4-125">*lpcbTotalAvailable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="498a4-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="498a4-126">Puntero a una variable que recibe el número total de bytes necesarios para almacenar la lista de recursos compartidos DDE de confianza.</span><span class="sxs-lookup"><span data-stu-id="498a4-126">A pointer to a variable that receives the total number of bytes needed to store the list of trusted DDE shares.</span></span> <span data-ttu-id="498a4-127">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="498a4-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="498a4-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="498a4-128">Return value</span></span>

<span data-ttu-id="498a4-129">Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.</span><span class="sxs-lookup"><span data-stu-id="498a4-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="498a4-130">Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="498a4-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="498a4-131">Si el parámetro *lpBuffer* es **null**, devuelve NDDE \_ BUF \_ demasiado \_ pequeño.</span><span class="sxs-lookup"><span data-stu-id="498a4-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="498a4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="498a4-132">Requirements</span></span>



| <span data-ttu-id="498a4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="498a4-133">Requirement</span></span> | <span data-ttu-id="498a4-134">Value</span><span class="sxs-lookup"><span data-stu-id="498a4-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="498a4-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="498a4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="498a4-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="498a4-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="498a4-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="498a4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="498a4-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="498a4-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="498a4-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="498a4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="498a4-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="498a4-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="498a4-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="498a4-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="498a4-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="498a4-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="498a4-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="498a4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="498a4-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="498a4-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="498a4-145">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="498a4-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="498a4-146">**NDdeTrustedShareEnumW** (Unicode) y **NDdeTrustedShareEnumA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="498a4-146">**NDdeTrustedShareEnumW** (Unicode) and **NDdeTrustedShareEnumA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="498a4-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="498a4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="498a4-148">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="498a4-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="498a4-149">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="498a4-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




