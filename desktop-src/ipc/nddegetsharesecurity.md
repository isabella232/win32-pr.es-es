---
description: Recupera el descriptor de seguridad asociado al recurso compartido DDE. Esto se hace normalmente para la edición.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Función NDdeGetShareSecurity (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912970"
---
# <a name="nddegetsharesecurity-function"></a><span data-ttu-id="1da6f-104">NDdeGetShareSecurity función)</span><span class="sxs-lookup"><span data-stu-id="1da6f-104">NDdeGetShareSecurity function</span></span>

<span data-ttu-id="1da6f-105">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="1da6f-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="1da6f-106">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="1da6f-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="1da6f-107">Recupera el descriptor de seguridad asociado al recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="1da6f-107">Retrieves the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="1da6f-108">Esto se hace normalmente para la edición.</span><span class="sxs-lookup"><span data-stu-id="1da6f-108">This is done usually for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da6f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1da6f-109">Syntax</span></span>


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
);
```



## <a name="parameters"></a><span data-ttu-id="1da6f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1da6f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1da6f-111">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1da6f-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da6f-112">Nombre del servidor en el que reside el DSDM.</span><span class="sxs-lookup"><span data-stu-id="1da6f-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="1da6f-113">*lpszShareName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1da6f-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da6f-114">Nombre del recurso compartido cuyo descriptor de seguridad se va a recuperar del DSDM.</span><span class="sxs-lookup"><span data-stu-id="1da6f-114">The name of the share whose security descriptor is to be retrieved from the DSDM.</span></span> <span data-ttu-id="1da6f-115">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1da6f-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1da6f-116">*si* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1da6f-116">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da6f-117">Valor [**de \_ información de seguridad**](/windows/desktop/SecAuthZ/security-information) que especifica la información de seguridad que se va a recuperar del descriptor de seguridad asociado al recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="1da6f-117">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that specifies the security information to be retrieved from the security descriptor associated with the share.</span></span>

</dd> <dt>

<span data-ttu-id="1da6f-118">*pSD* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1da6f-118">*pSD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1da6f-119">Puntero a una estructura [**de \_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que recibe el descriptor de seguridad autorelativo.</span><span class="sxs-lookup"><span data-stu-id="1da6f-119">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that receives the self-relative security descriptor.</span></span> <span data-ttu-id="1da6f-120">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1da6f-120">This parameter can be **NULL**.</span></span> <span data-ttu-id="1da6f-121">Si este parámetro es **null**, el DSDM determina el tamaño de la información de seguridad solicitada y devuelve el número de bytes necesarios en el parámetro *lpcbsdRequired* junto con el código de error de NDDE \_ BUF \_ demasiado \_ pequeño.</span><span class="sxs-lookup"><span data-stu-id="1da6f-121">If this parameter is **NULL**, the DSDM determines the size of the requested security information and returns the number of bytes needed in the *lpcbsdRequired* parameter along with the NDDE\_BUF\_TOO\_SMALL error code.</span></span>

</dd> <dt>

<span data-ttu-id="1da6f-122">*cbSD* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1da6f-122">*cbSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da6f-123">Tamaño del búfer *pSD* .</span><span class="sxs-lookup"><span data-stu-id="1da6f-123">The size of the *pSD* buffer.</span></span> <span data-ttu-id="1da6f-124">Este parámetro debe ser cero si *pSD* es **null**.</span><span class="sxs-lookup"><span data-stu-id="1da6f-124">This parameter must be zero if *pSD* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1da6f-125">*lpcbsdRequired* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1da6f-125">*lpcbsdRequired* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1da6f-126">Puntero a la variable que recibe el tamaño real del descriptor de seguridad recuperado.</span><span class="sxs-lookup"><span data-stu-id="1da6f-126">A pointer to the variable that receives the actual size of the retrieved security descriptor.</span></span> <span data-ttu-id="1da6f-127">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1da6f-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1da6f-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1da6f-128">Return value</span></span>

<span data-ttu-id="1da6f-129">Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.</span><span class="sxs-lookup"><span data-stu-id="1da6f-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="1da6f-130">Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="1da6f-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="1da6f-131">Si el parámetro *pSD* era **null**, devolverá NDDE \_ BUF \_ demasiado \_ pequeño.</span><span class="sxs-lookup"><span data-stu-id="1da6f-131">If the *pSD* parameter was **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1da6f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1da6f-132">Requirements</span></span>



| <span data-ttu-id="1da6f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1da6f-133">Requirement</span></span> | <span data-ttu-id="1da6f-134">Value</span><span class="sxs-lookup"><span data-stu-id="1da6f-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1da6f-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1da6f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1da6f-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1da6f-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1da6f-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1da6f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1da6f-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1da6f-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1da6f-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1da6f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1da6f-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1da6f-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="1da6f-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1da6f-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="1da6f-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1da6f-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1da6f-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1da6f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1da6f-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1da6f-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="1da6f-145">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1da6f-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1da6f-146">**NDdeGetShareSecurityW** (Unicode) y **NDdeGetShareSecurityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1da6f-146">**NDdeGetShareSecurityW** (Unicode) and **NDdeGetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="1da6f-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="1da6f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da6f-148">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="1da6f-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="1da6f-149">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="1da6f-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="1da6f-150">**información de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="1da6f-150">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="1da6f-151">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="1da6f-151">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> </dl>

 

