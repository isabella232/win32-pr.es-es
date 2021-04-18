---
title: Estructura de STOWED_EXCEPTION_INFORMATION_V2
description: Contiene información de excepción estibada.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- Estructura de STOWED_EXCEPTION_INFORMATION_V2 Informe de errores de Windows
- PSTOWED_EXCEPTION_INFORMATION_V2 puntero de estructura Informe de errores de Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705181"
---
# <a name="stowed_exception_information_v2-structure"></a><span data-ttu-id="06378-105">Estructura de la información de excepción de la \_ \_ \_ versión V2</span><span class="sxs-lookup"><span data-stu-id="06378-105">STOWED\_EXCEPTION\_INFORMATION\_V2 structure</span></span>

<span data-ttu-id="06378-106">Contiene información de excepción estibada.</span><span class="sxs-lookup"><span data-stu-id="06378-106">Contains stowed exception info.</span></span>

## <a name="syntax"></a><span data-ttu-id="06378-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06378-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a><span data-ttu-id="06378-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="06378-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="06378-109">**Header**</span><span class="sxs-lookup"><span data-stu-id="06378-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="06378-110">Tipo: **[ **\_ \_ \_ encabezado de información de excepción estibada**](stowed-exception-information-header.md)**</span><span class="sxs-lookup"><span data-stu-id="06378-110">Type: **[**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-111">La estructura de [**encabezado de \_ información de excepción \_ \_ estibada**](stowed-exception-information-header.md) que contiene información para esta estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="06378-111">The [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) structure that contains info for this parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="06378-112">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="06378-112">**ResultCode**</span></span>
</dt> <dd>

<span data-ttu-id="06378-113">Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06378-113">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-114">Código [**HRESULT**](/windows/desktop/WinProg/windows-data-types) para la excepción estibada.</span><span class="sxs-lookup"><span data-stu-id="06378-114">The [**HRESULT**](/windows/desktop/WinProg/windows-data-types) code for the stowed exception.</span></span>

</dd> <dt>

<span data-ttu-id="06378-115">**ExceptionForm**</span><span class="sxs-lookup"><span data-stu-id="06378-115">**ExceptionForm**</span></span>
</dt> <dd>

<span data-ttu-id="06378-116">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06378-116">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-117">Valor de 2 bits que identifica el formato de la excepción.</span><span class="sxs-lookup"><span data-stu-id="06378-117">A 2-bit value that identifies the form of the exception.</span></span>



| <span data-ttu-id="06378-118">Value</span><span class="sxs-lookup"><span data-stu-id="06378-118">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="06378-119">Significado</span><span class="sxs-lookup"><span data-stu-id="06378-119">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <span data-ttu-id="06378-120"><dt>**\_ Estibada Formulario de excepción \_ \_ binario**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="06378-120"><dt>**STOWED\_EXCEPTION\_FORM\_BINARY**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="06378-121">Este valor indica que el formato de la excepción es binario.</span><span class="sxs-lookup"><span data-stu-id="06378-121">This value indicates that the form of the exception is binary.</span></span><br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <span data-ttu-id="06378-122"><dt>**\_ Estibada \_ \_ Texto del formulario de excepción**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="06378-122"><dt>**STOWED\_EXCEPTION\_FORM\_TEXT**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="06378-123">Este valor indica que el formato de la excepción es texto.</span><span class="sxs-lookup"><span data-stu-id="06378-123">This value indicates that the form of the exception is text.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="06378-124">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="06378-124">**ThreadId**</span></span>
</dt> <dd>

<span data-ttu-id="06378-125">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06378-125">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-126">Un valor de 30 bits que identifica el subproceso que ha generado la excepción.</span><span class="sxs-lookup"><span data-stu-id="06378-126">A 30-bit value that identifies the thread that raised the exception.</span></span> <span data-ttu-id="06378-127">El valor se desplaza a la derecha 2 bits cuando se almacena.</span><span class="sxs-lookup"><span data-stu-id="06378-127">The value is shifted to the right by 2 bits when it's stored.</span></span> <span data-ttu-id="06378-128">Para volver a convertirlo en un identificador de subproceso válido, desplace el valor a la izquierda en 2.</span><span class="sxs-lookup"><span data-stu-id="06378-128">To convert it back to a valid thread ID, shift the value to the left by 2.</span></span> <span data-ttu-id="06378-129">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="06378-129">For example:</span></span>

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

<span data-ttu-id="06378-130">(*struct sin nombre*)</span><span class="sxs-lookup"><span data-stu-id="06378-130">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="06378-131">Los miembros de esta estructura anidada solo son válidos si el miembro **ExceptionForm** se establece en un **\_ \_ \_ archivo binario de formulario de excepción estibada**.</span><span class="sxs-lookup"><span data-stu-id="06378-131">The members of this nested structure are valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_BINARY**.</span></span>

<dl> <dt>

<span data-ttu-id="06378-132">**ExceptionAddress**</span><span class="sxs-lookup"><span data-stu-id="06378-132">**ExceptionAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06378-133">Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06378-133">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-134">Puntero que contiene la dirección de la excepción.</span><span class="sxs-lookup"><span data-stu-id="06378-134">A pointer that contains the exception address.</span></span>

</dd> <dt>

<span data-ttu-id="06378-135">**StackTraceWordSize**</span><span class="sxs-lookup"><span data-stu-id="06378-135">**StackTraceWordSize**</span></span>
</dt> <dd>

<span data-ttu-id="06378-136">Tipo: **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06378-136">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-137">Tamaño, en bytes, de cada palabra del seguimiento de la pila al que apunta el miembro **StackTrace** .</span><span class="sxs-lookup"><span data-stu-id="06378-137">Size, in bytes, of each word in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="06378-138">Este valor se establece en 4 para las plataformas de 32 bits y 8 para las plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="06378-138">This value is set to 4 for 32-bit platforms and 8 for 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="06378-139">**StackTraceWords**</span><span class="sxs-lookup"><span data-stu-id="06378-139">**StackTraceWords**</span></span>
</dt> <dd>

<span data-ttu-id="06378-140">Tipo: **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06378-140">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-141">El número de palabras del seguimiento de la pila al que apunta el miembro **StackTrace** .</span><span class="sxs-lookup"><span data-stu-id="06378-141">The number of words in the stack trace that the **StackTrace** member points to.</span></span> <span data-ttu-id="06378-142">El número de palabras es igual al número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="06378-142">The number of words is equal to the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="06378-143">**StackTrace**</span><span class="sxs-lookup"><span data-stu-id="06378-143">**StackTrace**</span></span>
</dt> <dd>

<span data-ttu-id="06378-144">Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06378-144">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-145">Un puntero a un bloque de memoria que contiene el seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="06378-145">A pointer to a memory block that contains the stack trace.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="06378-146">(*struct sin nombre*)</span><span class="sxs-lookup"><span data-stu-id="06378-146">(*unnamed struct*)</span></span>
</dt> <dd>

<span data-ttu-id="06378-147">El miembro de esta estructura anidada solo es válido si el miembro **ExceptionForm** está establecido en **texto de \_ \_ formulario de \_ excepción estibada**.</span><span class="sxs-lookup"><span data-stu-id="06378-147">The member of this nested structure is valid only if the **ExceptionForm** member is set to **STOWED\_EXCEPTION\_FORM\_TEXT**.</span></span>

<dl> <dt>

<span data-ttu-id="06378-148">**ErrorText**</span><span class="sxs-lookup"><span data-stu-id="06378-148">**ErrorText**</span></span>
</dt> <dd>

<span data-ttu-id="06378-149">Tipo: **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06378-149">Type: **[**PWSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-150">Un puntero a una cadena terminada en null que contiene el texto del error de la excepción.</span><span class="sxs-lookup"><span data-stu-id="06378-150">A pointer to a null-terminated string that contains the error text of the exception.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="06378-151">**NestedExceptionType**</span><span class="sxs-lookup"><span data-stu-id="06378-151">**NestedExceptionType**</span></span>
</dt> <dd>

<span data-ttu-id="06378-152">Tipo: **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06378-152">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-153">Valor de 32 bits que especifica el tipo de objeto al que apunta el miembro **NestedException** .</span><span class="sxs-lookup"><span data-stu-id="06378-153">A 32-bit value that specifies the type of object that the **NestedException** member points to.</span></span> <span data-ttu-id="06378-154">Defina el valor con esta macro de definición de tipo de intercambio de bytes que presupone Little-Endian:</span><span class="sxs-lookup"><span data-stu-id="06378-154">Define the value with this byte swap type-definition macro that assumes little-endian:</span></span>

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

<span data-ttu-id="06378-155">Estas son algunas definiciones de tipos comunes:</span><span class="sxs-lookup"><span data-stu-id="06378-155">Here are some common type definitions:</span></span>



| <span data-ttu-id="06378-156">Value</span><span class="sxs-lookup"><span data-stu-id="06378-156">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="06378-157">Significado</span><span class="sxs-lookup"><span data-stu-id="06378-157">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <span data-ttu-id="06378-158"><dt>**\_ Estibada \_Tipo anidado de excepción \_ \_ ninguno**</dt> <dt>(0x00000000)</dt></span><span class="sxs-lookup"><span data-stu-id="06378-158"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_NONE**</dt> <dt>(0x00000000)</dt></span></span> </dl>                                  | <span data-ttu-id="06378-159">Este valor especifica que no hay ningún objeto de excepción anidado.</span><span class="sxs-lookup"><span data-stu-id="06378-159">This value specifies that there is no nested exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <span data-ttu-id="06378-160"><dt>**\_ Estibada \_Tipo anidado \_ de \_ excepción**</dt> tipo <dt>anidado de excepción Win32 estibada \_ \_ \_ (' W32E ')</dt></span><span class="sxs-lookup"><span data-stu-id="06378-160"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_WIN32**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('W32E')</dt></span></span> </dl>    | <span data-ttu-id="06378-161">Este valor especifica que el miembro **NestedException** señala a un objeto de [**\_ registro de excepción**](/windows/desktop/api/winnt/ns-winnt-exception_record) .</span><span class="sxs-lookup"><span data-stu-id="06378-161">This value specifies that the **NestedException** member points to an [**EXCEPTION\_RECORD**](/windows/desktop/api/winnt/ns-winnt-exception_record) object.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <span data-ttu-id="06378-162"><dt>**\_ Estibada tipo \_ \_ \_ anidado**</dt> de excepción de tipo anidado de <dt>excepción estibada \_ \_ \_ (' estiba ')</dt></span><span class="sxs-lookup"><span data-stu-id="06378-162"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_STOWED**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('STOW')</dt></span></span> </dl> | <span data-ttu-id="06378-163">Este valor especifica que el miembro **NestedException** señala a otro objeto de excepción estibada.</span><span class="sxs-lookup"><span data-stu-id="06378-163">This value specifies that the **NestedException** member points to another stowed exception object.</span></span> <span data-ttu-id="06378-164">El otro objeto de excepción estibada puede ser un objeto de **\_ información de excepción de \_ \_ V2** u otra versión con un miembro de **encabezado** válido, es decir, un miembro de **encabezado** que contenga un encabezado de [**\_ información de excepción \_ \_ estibada**](stowed-exception-information-header.md)válido.</span><span class="sxs-lookup"><span data-stu-id="06378-164">The other stowed exception object can be a **STOWED\_EXCEPTION\_INFORMATION\_V2** object or a different version with a valid **Header** member, that is, a **Header** member that contains a valid [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md).</span></span><br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <span data-ttu-id="06378-165"><dt>**\_ Estibada Tipo \_ anidado \_ \_**</dt> de excepción tipo <dt>anidado de excepción CLR estibada \_ \_ \_ (' archivo clr1 ')</dt></span><span class="sxs-lookup"><span data-stu-id="06378-165"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_CLR**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('CLR1')</dt></span></span> </dl>          | <span data-ttu-id="06378-166">Este valor especifica que el miembro **NestedException** señala a un objeto de excepción ' archivo clr1 '.</span><span class="sxs-lookup"><span data-stu-id="06378-166">This value specifies that the **NestedException** member points to a 'CLR1' exception object.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <span data-ttu-id="06378-167"><dt>**\_ Estibada Tipo \_ anidado \_ \_**</dt> de excepción <dt> \_ \_ tipo anidado de excepción \_ (' LEO1 ')</dt></span><span class="sxs-lookup"><span data-stu-id="06378-167"><dt>**STOWED\_EXCEPTION\_NESTED\_TYPE\_LEO**</dt> <dt>STOWED\_EXCEPTION\_NESTED\_TYPE('LEO1')</dt></span></span> </dl>          | <span data-ttu-id="06378-168">Este valor especifica que el miembro **NestedException** señala a un objeto de excepción de idioma.</span><span class="sxs-lookup"><span data-stu-id="06378-168">This value specifies that the **NestedException** member points to a language exception object.</span></span><br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="06378-169">**NestedException**</span><span class="sxs-lookup"><span data-stu-id="06378-169">**NestedException**</span></span>
</dt> <dd>

<span data-ttu-id="06378-170">Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06378-170">Type: **[**PVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="06378-171">Un puntero a un tipo de excepción anidada.</span><span class="sxs-lookup"><span data-stu-id="06378-171">A pointer to a nested exception type.</span></span> <span data-ttu-id="06378-172">El miembro **NestedExceptionType** indica el tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="06378-172">The type of object is indicated by the **NestedExceptionType** member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06378-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06378-173">Remarks</span></span>

<span data-ttu-id="06378-174">**\_ Estibada La \_ información \_ de excepción V2** y el [**\_ encabezado de \_ información \_ de excepción estibada**](stowed-exception-information-header.md) no se definen actualmente en un encabezado que está disponible públicamente, por lo que debe definirlos en el código fuente antes de usarlos.</span><span class="sxs-lookup"><span data-stu-id="06378-174">**STOWED\_EXCEPTION\_INFORMATION\_V2** and [**STOWED\_EXCEPTION\_INFORMATION\_HEADER**](stowed-exception-information-header.md) currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="06378-175">La estructura V1 de la **\_ información de excepción \_ \_ estibada** es idéntica a esta estructura, salvo que no contiene los miembros **NestedExceptionType** y **NestedException** .</span><span class="sxs-lookup"><span data-stu-id="06378-175">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="06378-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06378-176">Requirements</span></span>



| <span data-ttu-id="06378-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="06378-177">Requirement</span></span> | <span data-ttu-id="06378-178">Value</span><span class="sxs-lookup"><span data-stu-id="06378-178">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="06378-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06378-179">Minimum supported client</span></span><br/> | <span data-ttu-id="06378-180">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="06378-180">Windows 8.1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="06378-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06378-181">Minimum supported server</span></span><br/> | <span data-ttu-id="06378-182">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="06378-182">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="06378-183">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06378-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="06378-184"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="06378-184"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06378-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="06378-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06378-186">**registro de excepción \_**</span><span class="sxs-lookup"><span data-stu-id="06378-186">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="06378-187">**encabezado de \_ información de excepción estibada \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06378-187">**STOWED\_EXCEPTION\_INFORMATION\_HEADER**</span></span>](stowed-exception-information-header.md)
</dt> </dl>

 

