---
description: Elimina un recurso compartido DDE del administrador de bases de datos de recursos compartidos DDE (DSDM).
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: Función NDdeShareDel (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686527"
---
# <a name="nddesharedel-function"></a><span data-ttu-id="7087e-103">NDdeShareDel función)</span><span class="sxs-lookup"><span data-stu-id="7087e-103">NDdeShareDel function</span></span>

<span data-ttu-id="7087e-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="7087e-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="7087e-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="7087e-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="7087e-106">Elimina un recurso compartido DDE del administrador de bases de datos de recursos compartidos DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="7087e-106">Deletes a DDE share from the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="7087e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7087e-107">Syntax</span></span>


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a><span data-ttu-id="7087e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7087e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7087e-109">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7087e-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7087e-110">Nombre del servidor cuyo DSDM se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="7087e-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="7087e-111">*lpszShareName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7087e-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7087e-112">Nombre del recurso compartido que se va a eliminar del DSDM.</span><span class="sxs-lookup"><span data-stu-id="7087e-112">The name of the share to be deleted from the DSDM.</span></span> <span data-ttu-id="7087e-113">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="7087e-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7087e-114">*wReserved* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7087e-114">*wReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7087e-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7087e-115">Reserved.</span></span> <span data-ttu-id="7087e-116">Este parámetro debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7087e-116">This parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7087e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7087e-117">Return value</span></span>

<span data-ttu-id="7087e-118">Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.</span><span class="sxs-lookup"><span data-stu-id="7087e-118">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="7087e-119">Si se produce un error en la función, el valor devuelto es un código de error que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="7087e-119">If the function fails, the return value is an error code which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7087e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7087e-120">Remarks</span></span>

<span data-ttu-id="7087e-121">Para eliminar un recurso compartido DDE de DSDM, debe tener el privilegio adecuado.</span><span class="sxs-lookup"><span data-stu-id="7087e-121">To delete a DDE share from the DSDM, you must have the appropriate privilege.</span></span> <span data-ttu-id="7087e-122">El creador del recurso compartido tiene privilegios de eliminación.</span><span class="sxs-lookup"><span data-stu-id="7087e-122">The share creator has delete privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="7087e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7087e-123">Requirements</span></span>



| <span data-ttu-id="7087e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7087e-124">Requirement</span></span> | <span data-ttu-id="7087e-125">Value</span><span class="sxs-lookup"><span data-stu-id="7087e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7087e-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7087e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7087e-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7087e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7087e-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7087e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7087e-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7087e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7087e-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7087e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7087e-131"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7087e-131"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="7087e-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7087e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="7087e-133"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7087e-133"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7087e-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7087e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7087e-135"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7087e-135"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="7087e-136">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="7087e-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7087e-137">**NDdeShareDelW** (Unicode) y **NDdeShareDelA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7087e-137">**NDdeShareDelW** (Unicode) and **NDdeShareDelA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="7087e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="7087e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7087e-139">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="7087e-139">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="7087e-140">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="7087e-140">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




