---
description: Recupera la lista de recursos compartidos DDE disponibles.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: Función NDdeShareEnum (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8bfa4884b88e72cb9a3b64bebf58af53cdc1047e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697429"
---
# <a name="nddeshareenum-function"></a><span data-ttu-id="166f3-103">NDdeShareEnum función)</span><span class="sxs-lookup"><span data-stu-id="166f3-103">NDdeShareEnum function</span></span>

<span data-ttu-id="166f3-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="166f3-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="166f3-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="166f3-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="166f3-106">Recupera la lista de recursos compartidos DDE disponibles.</span><span class="sxs-lookup"><span data-stu-id="166f3-106">Retrieves the list of available DDE shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="166f3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="166f3-107">Syntax</span></span>


```C++
UINT NDdeShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="166f3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="166f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="166f3-109">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="166f3-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="166f3-110">Nombre del servidor en el que reside el DSDM.</span><span class="sxs-lookup"><span data-stu-id="166f3-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-111">*nLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="166f3-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="166f3-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="166f3-112">Reserved.</span></span> <span data-ttu-id="166f3-113">Este parámetro debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="166f3-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-114">*lpBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="166f3-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="166f3-115">Un puntero a un búfer que recibe la lista de recursos compartidos DDE.</span><span class="sxs-lookup"><span data-stu-id="166f3-115">A pointer to a buffer that receives the list of DDE shares.</span></span> <span data-ttu-id="166f3-116">La lista de recursos compartidos DDE se almacena como una secuencia de cadenas separadas por null que finalizan con un carácter nulo doble al final.</span><span class="sxs-lookup"><span data-stu-id="166f3-116">The list of DDE shares is stored as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="166f3-117">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="166f3-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="166f3-118">Si *lpBuffer* es **null**, el DSDM devuelve el tamaño del búfer necesario para contener la lista de recursos compartidos en el parámetro *lpcbTotalAvailable* .</span><span class="sxs-lookup"><span data-stu-id="166f3-118">If *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-119">*cBufSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="166f3-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="166f3-120">Tamaño del búfer de *lpBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="166f3-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="166f3-121">Este parámetro debe ser cero si *lpBuffer* es **null**.</span><span class="sxs-lookup"><span data-stu-id="166f3-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-122">*lpnEntriesRead* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="166f3-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="166f3-123">Puntero a una variable que recibe el número total de recursos compartidos que se están enumerando.</span><span class="sxs-lookup"><span data-stu-id="166f3-123">A pointer to a variable that receives the total number of shares being enumerated.</span></span> <span data-ttu-id="166f3-124">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="166f3-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="166f3-125">*lpcbTotalAvailable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="166f3-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="166f3-126">Puntero a una variable que recibe el número total de bytes necesarios en el búfer para almacenar la lista de recursos compartidos DDE.</span><span class="sxs-lookup"><span data-stu-id="166f3-126">A pointer to a variable that receives the total number of bytes needed in the buffer to store the list of DDE shares.</span></span> <span data-ttu-id="166f3-127">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="166f3-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="166f3-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="166f3-128">Return value</span></span>

<span data-ttu-id="166f3-129">Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.</span><span class="sxs-lookup"><span data-stu-id="166f3-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="166f3-130">Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="166f3-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="166f3-131">Si el parámetro *lpBuffer* es **null**, devuelve NDDE \_ BUF \_ demasiado \_ pequeño.</span><span class="sxs-lookup"><span data-stu-id="166f3-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="166f3-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="166f3-132">Requirements</span></span>



| <span data-ttu-id="166f3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="166f3-133">Requirement</span></span> | <span data-ttu-id="166f3-134">Value</span><span class="sxs-lookup"><span data-stu-id="166f3-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="166f3-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="166f3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="166f3-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="166f3-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="166f3-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="166f3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="166f3-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="166f3-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="166f3-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="166f3-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="166f3-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="166f3-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="166f3-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="166f3-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="166f3-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="166f3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="166f3-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="166f3-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="166f3-145">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="166f3-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="166f3-146">**NDdeShareEnumW** (Unicode) y **NDdeShareEnumA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="166f3-146">**NDdeShareEnumW** (Unicode) and **NDdeShareEnumA** (ANSI)</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="166f3-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="166f3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="166f3-148">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="166f3-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="166f3-149">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="166f3-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




