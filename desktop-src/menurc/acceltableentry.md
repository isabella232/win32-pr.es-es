---
title: Estructura ACCELTABLEENTRY
description: Describe los datos de un recurso de tabla de aceleradores individual. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Menús de la estructura ACCELTABLEENTRY y otros recursos
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492976"
---
# <a name="acceltableentry-structure"></a><span data-ttu-id="0c111-105">Estructura ACCELTABLEENTRY</span><span class="sxs-lookup"><span data-stu-id="0c111-105">ACCELTABLEENTRY structure</span></span>

<span data-ttu-id="0c111-106">Describe los datos de un recurso de tabla de aceleradores individual.</span><span class="sxs-lookup"><span data-stu-id="0c111-106">Describes the data in an individual accelerator table resource.</span></span> <span data-ttu-id="0c111-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="0c111-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c111-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c111-108">Syntax</span></span>


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a><span data-ttu-id="0c111-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c111-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c111-110">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="0c111-110">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0c111-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="0c111-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0c111-112">Describe las características del acelerador del teclado.</span><span class="sxs-lookup"><span data-stu-id="0c111-112">Describes keyboard accelerator characteristics.</span></span> <span data-ttu-id="0c111-113">Este miembro puede tener uno o varios de los valores siguientes de Winuser. h.</span><span class="sxs-lookup"><span data-stu-id="0c111-113">This member can have one or more of the following values from Winuser.h.</span></span>



| <span data-ttu-id="0c111-114">Value</span><span class="sxs-lookup"><span data-stu-id="0c111-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="0c111-115">Significado</span><span class="sxs-lookup"><span data-stu-id="0c111-115">Meaning</span></span>                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <span data-ttu-id="0c111-116"><dt>**FVIRTKEY**</dt> <dt>true</dt></span><span class="sxs-lookup"><span data-stu-id="0c111-116"><dt>**FVIRTKEY**</dt> <dt>TRUE</dt></span></span> </dl>    | <span data-ttu-id="0c111-117">La tecla de aceleración es un [código de tecla virtual](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="0c111-117">The accelerator key is a [virtual-key code](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="0c111-118">Si no se especifica esta marca, se supone que la tecla de aceleración especifica un código de carácter ASCII.</span><span class="sxs-lookup"><span data-stu-id="0c111-118">If this flag is not specified, the accelerator key is assumed to specify an ASCII character code.</span></span> <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <span data-ttu-id="0c111-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="0c111-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="0c111-120">Los elementos de menú de la barra de menús no se resaltan cuando se utiliza un acelerador.</span><span class="sxs-lookup"><span data-stu-id="0c111-120">A menu item on the menu bar is not highlighted when an accelerator is used.</span></span> <span data-ttu-id="0c111-121">Este atributo está obsoleto y solo se conserva por compatibilidad con versiones anteriores de los archivos de recursos diseñados para Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0c111-121">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span><br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <span data-ttu-id="0c111-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="0c111-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="0c111-123">El acelerador solo se activa si el usuario presiona la tecla Mayús.</span><span class="sxs-lookup"><span data-stu-id="0c111-123">The accelerator is activated only if the user presses the SHIFT key.</span></span> <span data-ttu-id="0c111-124">Esta marca solo se aplica a las claves virtuales.</span><span class="sxs-lookup"><span data-stu-id="0c111-124">This flag applies only to virtual keys.</span></span> <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <span data-ttu-id="0c111-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="0c111-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span></span> </dl>    | <span data-ttu-id="0c111-126">El acelerador solo se activa si el usuario presiona la tecla CTRL.</span><span class="sxs-lookup"><span data-stu-id="0c111-126">The accelerator is activated only if the user presses the CTRL key.</span></span> <span data-ttu-id="0c111-127">Esta marca solo se aplica a las claves virtuales.</span><span class="sxs-lookup"><span data-stu-id="0c111-127">This flag applies only to virtual keys.</span></span> <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <span data-ttu-id="0c111-128"><dt>**FALT**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="0c111-128"><dt>**FALT**</dt> <dt>0x10</dt></span></span> </dl>                | <span data-ttu-id="0c111-129">El acelerador solo se activa si el usuario presiona la tecla ALT.</span><span class="sxs-lookup"><span data-stu-id="0c111-129">The accelerator is activated only if the user presses the ALT key.</span></span> <span data-ttu-id="0c111-130">Esta marca solo se aplica a las claves virtuales.</span><span class="sxs-lookup"><span data-stu-id="0c111-130">This flag applies only to virtual keys.</span></span> <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <span data-ttu-id="0c111-131"><dt>**0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="0c111-131"><dt>**0x80**</dt></span></span> </dl>                                                                          | <span data-ttu-id="0c111-132">La entrada es la última de una tabla de aceleradores.</span><span class="sxs-lookup"><span data-stu-id="0c111-132">The entry is last in an accelerator table.</span></span> <br/>                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="0c111-133">**wAnsi**</span><span class="sxs-lookup"><span data-stu-id="0c111-133">**wAnsi**</span></span>
</dt> <dd>

<span data-ttu-id="0c111-134">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="0c111-134">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0c111-135">Un valor de carácter ANSI o un código de tecla virtual que identifica la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="0c111-135">An ANSI character value or a virtual-key code that identifies the accelerator key.</span></span>

</dd> <dt>

<span data-ttu-id="0c111-136">**wId**</span><span class="sxs-lookup"><span data-stu-id="0c111-136">**wId**</span></span>
</dt> <dd>

<span data-ttu-id="0c111-137">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="0c111-137">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0c111-138">Identificador de la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="0c111-138">An identifier for the keyboard accelerator.</span></span> <span data-ttu-id="0c111-139">Este es el valor que se pasa al procedimiento de ventana cuando el usuario presiona la tecla especificada.</span><span class="sxs-lookup"><span data-stu-id="0c111-139">This is the value passed to the window procedure when the user presses the specified key.</span></span>

</dd> <dt>

<span data-ttu-id="0c111-140">**padding**</span><span class="sxs-lookup"><span data-stu-id="0c111-140">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="0c111-141">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="0c111-141">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0c111-142">Número de bytes insertados para asegurarse de que la estructura está alineada en un límite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0c111-142">The number of bytes inserted to ensure that the structure is aligned on a **DWORD** boundary.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c111-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c111-143">Remarks</span></span>

<span data-ttu-id="0c111-144">La estructura **ACCELTABLEENTRY** se repite para todas las entradas de la tabla de aceleradores en el recurso.</span><span class="sxs-lookup"><span data-stu-id="0c111-144">The **ACCELTABLEENTRY** structure is repeated for all accelerator table entries in the resource.</span></span> <span data-ttu-id="0c111-145">La última entrada de la tabla se marca con el valor 0x0080.</span><span class="sxs-lookup"><span data-stu-id="0c111-145">The last entry in the table is flagged with the value 0x0080.</span></span>

<span data-ttu-id="0c111-146">Puede calcular el número de elementos de la tabla si divide la longitud del recurso por ocho.</span><span class="sxs-lookup"><span data-stu-id="0c111-146">You can compute the number of elements in the table if you divide the length of the resource by eight.</span></span> <span data-ttu-id="0c111-147">A continuación, la aplicación puede tener acceso de forma aleatoria a las entradas individuales de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="0c111-147">Then your application can randomly access the individual fixed-length entries.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c111-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c111-148">Requirements</span></span>



| <span data-ttu-id="0c111-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c111-149">Requirement</span></span> | <span data-ttu-id="0c111-150">Value</span><span class="sxs-lookup"><span data-stu-id="0c111-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0c111-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c111-151">Minimum supported client</span></span><br/> | <span data-ttu-id="0c111-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0c111-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0c111-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c111-153">Minimum supported server</span></span><br/> | <span data-ttu-id="0c111-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c111-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0c111-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c111-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c111-156">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0c111-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0c111-157">**CreateAcceleratorTable**</span><span class="sxs-lookup"><span data-stu-id="0c111-157">**CreateAcceleratorTable**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

<span data-ttu-id="0c111-158">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0c111-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0c111-159">Recursos</span><span class="sxs-lookup"><span data-stu-id="0c111-159">Resources</span></span>](resources.md)
</dt> </dl>

 

