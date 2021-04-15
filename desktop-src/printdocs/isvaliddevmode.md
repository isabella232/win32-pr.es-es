---
description: La función IsValidDevmode comprueba que el contenido de una estructura DEVMODE es válido.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Función IsValidDevmode (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720729"
---
# <a name="isvaliddevmode-function"></a><span data-ttu-id="062ca-103">IsValidDevmode función)</span><span class="sxs-lookup"><span data-stu-id="062ca-103">IsValidDevmode function</span></span>

<span data-ttu-id="062ca-104">La función **IsValidDevmode** comprueba que el contenido de una estructura DEVMODE es válido.</span><span class="sxs-lookup"><span data-stu-id="062ca-104">The **IsValidDevmode** function verifies that the contents of a DEVMODE structure are valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="062ca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="062ca-105">Syntax</span></span>


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a><span data-ttu-id="062ca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="062ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="062ca-107">*pDevmode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="062ca-107">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="062ca-108">Puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="062ca-108">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to validate.</span></span>

</dd> <dt>

<span data-ttu-id="062ca-109">*DevmodeSize*</span><span class="sxs-lookup"><span data-stu-id="062ca-109">*DevmodeSize*</span></span> 
</dt> <dd>

<span data-ttu-id="062ca-110">Tamaño en bytes del búfer de bytes de entrada.</span><span class="sxs-lookup"><span data-stu-id="062ca-110">The size in bytes of the input byte buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="062ca-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="062ca-111">Return value</span></span>

<span data-ttu-id="062ca-112">**True**, si la [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) es estructuralmente válida.</span><span class="sxs-lookup"><span data-stu-id="062ca-112">**TRUE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is structurally valid.</span></span> <span data-ttu-id="062ca-113">Si se encuentran errores menores, la función los corregirá y devolverá **true**.</span><span class="sxs-lookup"><span data-stu-id="062ca-113">If minor errors are found the function will fix them and return **TRUE**.</span></span>

<span data-ttu-id="062ca-114">**False**, si [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) tiene uno o más problemas estructurales importantes.</span><span class="sxs-lookup"><span data-stu-id="062ca-114">**FALSE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) has one or more significant structural problems.</span></span> <span data-ttu-id="062ca-115">Por ejemplo, su miembro **dmSize** está mal alineado o especifica un búfer demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="062ca-115">For example, its **dmSize** member is misaligned or specifies a buffer that is too small.</span></span> <span data-ttu-id="062ca-116">Además, **false** si **pDevmode** es **null**.</span><span class="sxs-lookup"><span data-stu-id="062ca-116">Also, **FALSE** if **pDevmode** is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="062ca-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="062ca-117">Remarks</span></span>

<span data-ttu-id="062ca-118">No se comprueban los campos de controlador de impresora privados de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , solo los campos públicos.</span><span class="sxs-lookup"><span data-stu-id="062ca-118">No private printer driver fields of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) are checked, only the public fields.</span></span>

<span data-ttu-id="062ca-119">Los autores de llamadas deben usar **dmSize** + **dmDriverExtra** para **DevmodeSize** solo si pueden garantizar que el tamaño del búfer de entrada sea al menos tan grande.</span><span class="sxs-lookup"><span data-stu-id="062ca-119">Callers should use **dmSize**+**dmDriverExtra** for **DevmodeSize** only if they can guarantee that the input buffer size is at least that big.</span></span> <span data-ttu-id="062ca-120">Dado que [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) normalmente es un dato que no es de confianza, los valores que se encuentran en el búfer de entrada en los desplazamientos **dmSize** y **dmDriverExtra** también son de confianza.</span><span class="sxs-lookup"><span data-stu-id="062ca-120">Since the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is generally untrusted data, the values that are in the input buffer at the **dmSize** and **dmDriverExtra** offsets are also untrusted.</span></span>

<span data-ttu-id="062ca-121">Esta función se ejecuta en el contexto de la cuenta de usuario Least-Privileged (LUA).</span><span class="sxs-lookup"><span data-stu-id="062ca-121">This function is executable in Least-Privileged User Account (LUA) context.</span></span>

## <a name="requirements"></a><span data-ttu-id="062ca-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="062ca-122">Requirements</span></span>



| <span data-ttu-id="062ca-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="062ca-123">Requirement</span></span> | <span data-ttu-id="062ca-124">Value</span><span class="sxs-lookup"><span data-stu-id="062ca-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="062ca-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="062ca-125">Minimum supported client</span></span><br/> | <span data-ttu-id="062ca-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="062ca-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="062ca-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="062ca-127">Minimum supported server</span></span><br/> | <span data-ttu-id="062ca-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="062ca-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="062ca-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="062ca-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="062ca-130"><dt>Winspool. h</dt></span><span class="sxs-lookup"><span data-stu-id="062ca-130"><dt>Winspool.h</dt></span></span> </dl>   |
| <span data-ttu-id="062ca-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="062ca-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="062ca-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="062ca-132"><dt>Winspool.lib</dt></span></span> </dl> |
| <span data-ttu-id="062ca-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="062ca-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="062ca-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="062ca-134"><dt>Winspool.drv</dt></span></span> </dl> |
| <span data-ttu-id="062ca-135">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="062ca-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="062ca-136">**IsValidDevmodeW** (Unicode) y **IsValidDevmodeA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="062ca-136">**IsValidDevmodeW** (Unicode) and **IsValidDevmodeA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="062ca-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="062ca-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="062ca-138">Impresión</span><span class="sxs-lookup"><span data-stu-id="062ca-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="062ca-139">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="062ca-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="062ca-140">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="062ca-140">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




