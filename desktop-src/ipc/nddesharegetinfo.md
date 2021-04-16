---
description: Recupera la información del recurso compartido DDE. Esto se suele hacer para editar.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Función NDdeShareGetInfo (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686526"
---
# <a name="nddesharegetinfo-function"></a><span data-ttu-id="f6e9b-104">NDdeShareGetInfo función)</span><span class="sxs-lookup"><span data-stu-id="f6e9b-104">NDdeShareGetInfo function</span></span>

<span data-ttu-id="f6e9b-105">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="f6e9b-106">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="f6e9b-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="f6e9b-107">Recupera la información del recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-107">Retrieves DDE share information.</span></span> <span data-ttu-id="f6e9b-108">Esto se suele hacer para editar.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-108">This is usually done for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e9b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6e9b-109">Syntax</span></span>


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a><span data-ttu-id="f6e9b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6e9b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6e9b-111">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6e9b-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6e9b-112">Nombre del servidor en el que reside el DSDM.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="f6e9b-113">*lpszShareName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6e9b-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6e9b-114">Nombre del recurso compartido cuya información se va a recuperar del DSDM.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-114">The share name whose information is to be retrieved from the DSDM.</span></span> <span data-ttu-id="f6e9b-115">Este parámetro no debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-115">This parameter must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f6e9b-116">*nLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6e9b-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6e9b-117">Nivel de información.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-117">The information level.</span></span> <span data-ttu-id="f6e9b-118">Este parámetro debe ser 2.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="f6e9b-119">*lpBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6e9b-119">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6e9b-120">Un puntero a un búfer que recibe la estructura [**NDDESHAREINFO**](nddeshareinfo-str.md) y los datos asociados a los que apuntan sus miembros.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-120">A pointer to a buffer that receives the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure and associated data pointed to by its members.</span></span> <span data-ttu-id="f6e9b-121">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-121">This parameter can be **NULL**.</span></span> <span data-ttu-id="f6e9b-122">Si *lpBuffer* es **null**, el DSDM calcula el número de bytes necesarios para almacenar la información de recurso compartido solicitada y devuelve ese valor en el campo *lpnTotalAvailable* junto con el \_ error de NDDE BUF \_ demasiado \_ pequeño.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-122">If *lpBuffer* is **NULL**, then the DSDM calculates the number of bytes required to store the requested share information and returns that value in the *lpnTotalAvailable* field along with the NDDE\_BUF\_TOO\_SMALL error.</span></span>

</dd> <dt>

<span data-ttu-id="f6e9b-123">*cBufSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6e9b-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6e9b-124">Tamaño del búfer de *lpBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-124">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="f6e9b-125">Si *lpBuffer* es **null**, *cBufSize* debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-125">If *lpBuffer* is **NULL**, then *cBufSize* should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f6e9b-126">*lpnTotalAvailable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6e9b-126">*lpnTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6e9b-127">Puntero a una variable que recibe el número total de bytes necesarios para almacenar la información de recurso compartido solicitada.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-127">A pointer to a variable that receives the total number of bytes needed to store the requested share information.</span></span> <span data-ttu-id="f6e9b-128">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-128">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f6e9b-129">*lpnItems* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6e9b-129">*lpnItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6e9b-130">Un puntero a una máscara de selección de elementos para la recuperación parcial de información de recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-130">A pointer to an item selection mask for partial share information retrieval.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6e9b-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6e9b-131">Return value</span></span>

<span data-ttu-id="f6e9b-132">Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-132">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="f6e9b-133">Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="f6e9b-133">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="f6e9b-134">Si el parámetro *lpBuffer* es **null**, devuelve NDDE \_ BUF \_ demasiado \_ pequeño.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-134">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6e9b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6e9b-135">Requirements</span></span>



| <span data-ttu-id="f6e9b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6e9b-136">Requirement</span></span> | <span data-ttu-id="f6e9b-137">Value</span><span class="sxs-lookup"><span data-stu-id="f6e9b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e9b-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6e9b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f6e9b-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f6e9b-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f6e9b-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6e9b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f6e9b-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f6e9b-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f6e9b-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6e9b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6e9b-143"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6e9b-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6e9b-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6e9b-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6e9b-145"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6e9b-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f6e9b-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6e9b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6e9b-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6e9b-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6e9b-148">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f6e9b-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f6e9b-149">**NDdeShareGetInfoW** (Unicode) y **NDdeShareGetInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f6e9b-149">**NDdeShareGetInfoW** (Unicode) and **NDdeShareGetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f6e9b-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6e9b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e9b-151">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="f6e9b-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="f6e9b-152">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="f6e9b-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="f6e9b-153">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="f6e9b-153">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="f6e9b-154">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="f6e9b-154">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> </dl>

 

 




