---
description: Traduce la cadena Unicode especificada en una nueva cadena de caracteres, usando la página de códigos del formato de transformación Unicode de 8 bits (UTF-8).
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Función RtlUnicodeToUTF8N (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152962"
---
# <a name="rtlunicodetoutf8n-function"></a><span data-ttu-id="b8637-103">RtlUnicodeToUTF8N función)</span><span class="sxs-lookup"><span data-stu-id="b8637-103">RtlUnicodeToUTF8N function</span></span>

<span data-ttu-id="b8637-104">Traduce la cadena Unicode especificada en una nueva cadena de caracteres, usando la página de códigos del formato de transformación Unicode de 8 bits (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="b8637-104">Translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8637-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8637-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="b8637-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8637-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8637-107">*UTF8StringDestination* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b8637-107">*UTF8StringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8637-108">Un puntero a un búfer asignado por el llamador para recibir la cadena traducida.</span><span class="sxs-lookup"><span data-stu-id="b8637-108">A pointer to a caller-allocated buffer to receive the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="b8637-109">*UTF8StringMaxByteCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8637-109">*UTF8StringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8637-110">Número máximo de bytes que se van a escribir en *UTF8StringDestination*.</span><span class="sxs-lookup"><span data-stu-id="b8637-110">Maximum number of bytes to be written to *UTF8StringDestination*.</span></span> <span data-ttu-id="b8637-111">Si este valor hace que la cadena traducida se trunque, **RtlUnicodeToUTF8N** devuelve un estado de error.</span><span class="sxs-lookup"><span data-stu-id="b8637-111">If this value causes the translated string to be truncated, **RtlUnicodeToUTF8N** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="b8637-112">*UTF8StringActualByteCount* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b8637-112">*UTF8StringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8637-113">Puntero a una variable asignada por el llamador que recibe la longitud, en bytes, de la cadena traducida.</span><span class="sxs-lookup"><span data-stu-id="b8637-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="b8637-114">Este parámetro es opcional y puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b8637-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="b8637-115">Si la cadena se trunca, el número devuelto cuenta el recuento de cadenas truncadas real.</span><span class="sxs-lookup"><span data-stu-id="b8637-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="b8637-116">*UnicodeStringSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8637-116">*UnicodeStringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8637-117">Puntero a la cadena de origen Unicode que se va a traducir.</span><span class="sxs-lookup"><span data-stu-id="b8637-117">A pointer to the Unicode source string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="b8637-118">\* UnicodeStringByteCount \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b8637-118">\*UnicodeStringByteCount \* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8637-119">Especifica el número de bytes de la cadena de origen Unicode a los que apunta el parámetro *UnicodeStringSource* .</span><span class="sxs-lookup"><span data-stu-id="b8637-119">Specifies the number of bytes in the Unicode source string that the *UnicodeStringSource* parameter points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8637-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8637-120">Return value</span></span>

<span data-ttu-id="b8637-121">**RtlUnicodeToUTF8N** devuelve uno de los siguientes valores de NTSTATUS:</span><span class="sxs-lookup"><span data-stu-id="b8637-121">**RtlUnicodeToUTF8N** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="b8637-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b8637-122">Return code</span></span>                                                                                                  | <span data-ttu-id="b8637-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8637-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8637-124"><dt>**ESTADO \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b8637-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="b8637-125">La cadena Unicode se convirtió a UTF-8.</span><span class="sxs-lookup"><span data-stu-id="b8637-125">The Unicode string was converted to UTF-8.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="b8637-126"><dt>**ESTADO \_ \_ no \_ asignado**</dt></span><span class="sxs-lookup"><span data-stu-id="b8637-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="b8637-127">Se encontró un carácter de entrada no válido y se ha reemplazado.</span><span class="sxs-lookup"><span data-stu-id="b8637-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="b8637-128">Este estado se considera un estado correcto.</span><span class="sxs-lookup"><span data-stu-id="b8637-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="b8637-129"><dt>**ESTADO \_ parámetro no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8637-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="b8637-130">Ambos punteros a *UTF8StringDestination* y *UTF8StringActualByteCount* eran **null**.</span><span class="sxs-lookup"><span data-stu-id="b8637-130">Both pointers to *UTF8StringDestination* and *UTF8StringActualByteCount* were **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="b8637-131"><dt>**Parámetro de estado \_ no válido \_ \_ 4**</dt></span><span class="sxs-lookup"><span data-stu-id="b8637-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="b8637-132">*UnicodeStringSource* era **null**.</span><span class="sxs-lookup"><span data-stu-id="b8637-132">The *UnicodeStringSource* was **NULL**.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="b8637-133"><dt>**búfer de estado \_ \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="b8637-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="b8637-134">*UTF8StringDestination* se truncó.</span><span class="sxs-lookup"><span data-stu-id="b8637-134">*UTF8StringDestination* was truncated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="b8637-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8637-135">Remarks</span></span>

<span data-ttu-id="b8637-136">Aunque *UTF8StringActualByteCount* es opcional y puede ser **null**, los llamadores deben proporcionar almacenamiento para él, ya que la longitud recibida se puede usar para determinar si la conversión se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b8637-136">Although *UTF8StringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span> <span data-ttu-id="b8637-137">Esta rutina no modifica la cadena de origen.</span><span class="sxs-lookup"><span data-stu-id="b8637-137">This routine does not modify the source string.</span></span> <span data-ttu-id="b8637-138">Devuelve una cadena UTF-8 terminada en NULL si el *UnicodeStringSource* dado incluye un terminador null y si el *UTF8StringMaxByteCount* determinado no ha provocado el truncamiento.</span><span class="sxs-lookup"><span data-stu-id="b8637-138">It returns a null-terminated UTF-8 string if the given *UnicodeStringSource* included a NULL terminator and if the given *UTF8StringMaxByteCount* did not cause truncation.</span></span>

<span data-ttu-id="b8637-139">Si el resultado se trunca y se encuentra un carácter de entrada no válido, la función devuelve un error de búfer de estado \_ \_ demasiado \_ pequeño.</span><span class="sxs-lookup"><span data-stu-id="b8637-139">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="b8637-140">Si *UTF8StringDestination* se establece en **null** , la función devolverá el número necesario de bytes para hospedar la cadena traducida sin ningún truncamiento en *UTF8StringActualByteCount*.</span><span class="sxs-lookup"><span data-stu-id="b8637-140">If the *UTF8StringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UTF8StringActualByteCount*.</span></span>

<span data-ttu-id="b8637-141">Los autores de llamadas de **RtlUnicodeToUTF8N** deben ejecutarse en el nivel de distribución de IRQL < \_ .</span><span class="sxs-lookup"><span data-stu-id="b8637-141">Callers of **RtlUnicodeToUTF8N** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8637-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8637-142">Requirements</span></span>



| <span data-ttu-id="b8637-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8637-143">Requirement</span></span> | <span data-ttu-id="b8637-144">Value</span><span class="sxs-lookup"><span data-stu-id="b8637-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8637-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8637-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b8637-146">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8637-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b8637-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8637-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b8637-148">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8637-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b8637-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8637-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8637-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8637-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="b8637-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8637-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8637-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8637-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8637-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8637-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8637-154">**RtlUTF8ToUnicodeN**</span><span class="sxs-lookup"><span data-stu-id="b8637-154">**RtlUTF8ToUnicodeN**</span></span>](rtlutf8tounicoden.md)
</dt> </dl>

 

 




