---
description: Establece el descriptor de seguridad asociado al recurso compartido DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Función NDdeSetShareSecurity (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687974"
---
# <a name="nddesetsharesecurity-function"></a><span data-ttu-id="d4ceb-103">NDdeSetShareSecurity función)</span><span class="sxs-lookup"><span data-stu-id="d4ceb-103">NDdeSetShareSecurity function</span></span>

<span data-ttu-id="d4ceb-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="d4ceb-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="d4ceb-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="d4ceb-106">Establece el descriptor de seguridad asociado al recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-106">Sets the security descriptor associated with the DDE share.</span></span> <span data-ttu-id="d4ceb-107">Esto se hace normalmente después de editar la DACL asignada al recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-107">This is done usually after editing the DACL assigned to the DDE share.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ceb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4ceb-108">Syntax</span></span>


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a><span data-ttu-id="d4ceb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4ceb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ceb-110">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4ceb-110">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ceb-111">Nombre del servidor cuyo DSDM se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-111">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="d4ceb-112">*lpszShareName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4ceb-112">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ceb-113">Nombre del recurso compartido cuyo descriptor de seguridad se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-113">The name of the share whose security descriptor is to be modified.</span></span> <span data-ttu-id="d4ceb-114">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d4ceb-115">*si* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4ceb-115">*si* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ceb-116">Valor [**de \_ información de seguridad**](/windows/desktop/SecAuthZ/security-information) que identifica la información de seguridad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-116">A [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information) value that identifies the security information to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d4ceb-117">*pSD* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4ceb-117">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ceb-118">Puntero a una estructura [**de \_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contiene información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-118">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains security information.</span></span> <span data-ttu-id="d4ceb-119">Este parámetro no puede ser **null** y debe apuntar a un descriptor de seguridad válido.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-119">This parameter cannot be **NULL** and should point to a valid security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ceb-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4ceb-120">Return value</span></span>

<span data-ttu-id="d4ceb-121">Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-121">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="d4ceb-122">Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="d4ceb-122">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4ceb-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4ceb-123">Remarks</span></span>

<span data-ttu-id="d4ceb-124">Para modificar el [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) asociado a un recurso compartido DDE en DSDM, el usuario debe tener el privilegio adecuado. el creador del recurso compartido tiene este privilegio.</span><span class="sxs-lookup"><span data-stu-id="d4ceb-124">To modify the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associated with a DDE share in the DSDM, the user must have appropriate privilege; the share creator has this privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ceb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4ceb-125">Requirements</span></span>



| <span data-ttu-id="d4ceb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4ceb-126">Requirement</span></span> | <span data-ttu-id="d4ceb-127">Value</span><span class="sxs-lookup"><span data-stu-id="d4ceb-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ceb-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4ceb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ceb-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d4ceb-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d4ceb-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4ceb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ceb-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4ceb-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d4ceb-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4ceb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4ceb-133"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ceb-133"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4ceb-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4ceb-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4ceb-135"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4ceb-135"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d4ceb-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4ceb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4ceb-137"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4ceb-137"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4ceb-138">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d4ceb-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d4ceb-139">**NDdeSetShareSecurityW** (Unicode) y **NDdeSetShareSecurityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d4ceb-139">**NDdeSetShareSecurityW** (Unicode) and **NDdeSetShareSecurityA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="d4ceb-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4ceb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ceb-141">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="d4ceb-141">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="d4ceb-142">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="d4ceb-142">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="d4ceb-143">**información de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="d4ceb-143">**SECURITY\_INFORMATION**</span></span>](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[<span data-ttu-id="d4ceb-144">**NDdeGetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="d4ceb-144">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)
</dt> </dl>

 

