---
description: Establece la información de recursos compartidos DDE. Normalmente, esto se realiza después de la edición.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Función NDdeShareSetInfo (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686525"
---
# <a name="nddesharesetinfo-function"></a><span data-ttu-id="6233d-104">NDdeShareSetInfo función)</span><span class="sxs-lookup"><span data-stu-id="6233d-104">NDdeShareSetInfo function</span></span>

<span data-ttu-id="6233d-105">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="6233d-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="6233d-106">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="6233d-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="6233d-107">Establece la información de recursos compartidos DDE.</span><span class="sxs-lookup"><span data-stu-id="6233d-107">Sets DDE share information.</span></span> <span data-ttu-id="6233d-108">Normalmente, esto se realiza después de la edición.</span><span class="sxs-lookup"><span data-stu-id="6233d-108">This is usually done after editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="6233d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6233d-109">Syntax</span></span>


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a><span data-ttu-id="6233d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6233d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6233d-111">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6233d-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6233d-112">Nombre del servidor cuyo DSDM se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="6233d-112">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="6233d-113">*lpszShareName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6233d-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6233d-114">Nombre del nombre del recurso compartido cuya información se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="6233d-114">The name of the share name whose information is to be modified.</span></span> <span data-ttu-id="6233d-115">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6233d-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6233d-116">*nLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6233d-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6233d-117">Nivel de información.</span><span class="sxs-lookup"><span data-stu-id="6233d-117">The information level.</span></span> <span data-ttu-id="6233d-118">Este parámetro debe ser 2.</span><span class="sxs-lookup"><span data-stu-id="6233d-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="6233d-119">*lpBuffer* \[in\]</span><span class="sxs-lookup"><span data-stu-id="6233d-119">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6233d-120">Puntero a la estructura [**NDDESHAREINFO**](nddeshareinfo-str.md) que especifica la información de recursos compartidos DDE que se va a almacenar en el DSDM.</span><span class="sxs-lookup"><span data-stu-id="6233d-120">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that specifies the DDE share information to be stored in the DSDM.</span></span> <span data-ttu-id="6233d-121">Actualmente, la información de los recursos compartidos DDE se modifica en su totalidad, es decir, no se realiza ninguna edición parcial.</span><span class="sxs-lookup"><span data-stu-id="6233d-121">Currently the DDE share information is modified as a whole, that is, no partial edits are made.</span></span> <span data-ttu-id="6233d-122">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6233d-122">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6233d-123">*cBufSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6233d-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6233d-124">Tamaño del búfer de *lpBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="6233d-124">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6233d-125">*sParmNum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6233d-125">*sParmNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6233d-126">Índice del parámetro que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="6233d-126">The parameter index to be modified.</span></span> <span data-ttu-id="6233d-127">La implementación actual no admite la modificación parcial; por lo tanto, este parámetro debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6233d-127">The current implementation does not support partial modification; therefore, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6233d-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6233d-128">Return value</span></span>

<span data-ttu-id="6233d-129">Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.</span><span class="sxs-lookup"><span data-stu-id="6233d-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="6233d-130">Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="6233d-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6233d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6233d-131">Requirements</span></span>



| <span data-ttu-id="6233d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6233d-132">Requirement</span></span> | <span data-ttu-id="6233d-133">Value</span><span class="sxs-lookup"><span data-stu-id="6233d-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6233d-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6233d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6233d-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6233d-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6233d-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6233d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6233d-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6233d-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6233d-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6233d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6233d-139"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6233d-139"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="6233d-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6233d-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="6233d-141"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6233d-141"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6233d-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6233d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6233d-143"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6233d-143"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="6233d-144">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="6233d-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6233d-145">**NDdeShareSetInfoW** (Unicode) y **NDdeShareSetInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6233d-145">**NDdeShareSetInfoW** (Unicode) and **NDdeShareSetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="6233d-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="6233d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6233d-147">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="6233d-147">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="6233d-148">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="6233d-148">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="6233d-149">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="6233d-149">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="6233d-150">**NDdeShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="6233d-150">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)
</dt> </dl>

 

 




