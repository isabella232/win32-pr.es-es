---
description: Convierte un código de error devuelto por una función DDE de red en una cadena de error que explica el código de error devuelto.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Función NDdeGetErrorString (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104081981"
---
# <a name="nddegeterrorstring-function"></a><span data-ttu-id="8a8f1-103">NDdeGetErrorString función)</span><span class="sxs-lookup"><span data-stu-id="8a8f1-103">NDdeGetErrorString function</span></span>

<span data-ttu-id="8a8f1-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="8a8f1-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="8a8f1-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="8a8f1-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="8a8f1-106">Convierte un código de error devuelto por una función DDE de red en una cadena de error que explica el código de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="8a8f1-106">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8f1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a8f1-107">Syntax</span></span>


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="8a8f1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a8f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a8f1-109">*uErrorCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a8f1-109">*uErrorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8f1-110">Código de error que se va a convertir en una cadena de error.</span><span class="sxs-lookup"><span data-stu-id="8a8f1-110">The error code to be converted into an error string.</span></span>

</dd> <dt>

<span data-ttu-id="8a8f1-111">*lpszErrorString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8a8f1-111">*lpszErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8f1-112">Puntero a un búfer que recibe la cadena de error traducida.</span><span class="sxs-lookup"><span data-stu-id="8a8f1-112">A pointer to a buffer that receives the translated error string.</span></span> <span data-ttu-id="8a8f1-113">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8a8f1-113">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="8a8f1-114">Si el búfer no es lo suficientemente grande como para almacenar la cadena de error completa, se trunca la cadena.</span><span class="sxs-lookup"><span data-stu-id="8a8f1-114">If the buffer is not large enough to store the complete error string, the string is truncated.</span></span>

</dd> <dt>

<span data-ttu-id="8a8f1-115">*cBufSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a8f1-115">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8f1-116">Tamaño del búfer para recibir la cadena de error, en **TCHARs**.</span><span class="sxs-lookup"><span data-stu-id="8a8f1-116">The size of the buffer to receive the error string, in **TCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a8f1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a8f1-117">Return value</span></span>

<span data-ttu-id="8a8f1-118">Si la función es correcta, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="8a8f1-118">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="8a8f1-119">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8a8f1-119">If the function fails, the return value is a nonzero error code.</span></span> <span data-ttu-id="8a8f1-120">Si el búfer de *lpszErrorString* no es lo suficientemente grande como para aceptar la cadena de error completa y se trunca la cadena, la función devuelve el valor NDDE \_ \_ error interno.</span><span class="sxs-lookup"><span data-stu-id="8a8f1-120">If the *lpszErrorString* buffer is not large enough to accept the complete error string, and the string is truncated, the function returns the value NDDE\_INTERNAL\_ERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a8f1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a8f1-121">Requirements</span></span>



| <span data-ttu-id="8a8f1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a8f1-122">Requirement</span></span> | <span data-ttu-id="8a8f1-123">Value</span><span class="sxs-lookup"><span data-stu-id="8a8f1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8f1-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a8f1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8a8f1-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8a8f1-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8a8f1-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a8f1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8a8f1-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a8f1-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a8f1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a8f1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a8f1-129"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a8f1-129"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a8f1-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a8f1-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a8f1-131"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a8f1-131"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8a8f1-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a8f1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a8f1-133"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8f1-133"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a8f1-134">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8a8f1-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8a8f1-135">**NDdeGetErrorStringW** (Unicode) y **NDdeGetErrorStringA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8a8f1-135">**NDdeGetErrorStringW** (Unicode) and **NDdeGetErrorStringA** (ANSI)</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="8a8f1-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a8f1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8f1-137">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="8a8f1-137">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="8a8f1-138">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="8a8f1-138">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




