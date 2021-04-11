---
description: Traduce la cadena de origen especificada en una cadena Unicode, usando la página de códigos del formato de transformación Unicode de 8 bits (UTF-8).
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: Función RtlUTF8ToUnicodeN (WDM. h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274905"
---
# <a name="rtlutf8tounicoden-function"></a><span data-ttu-id="64b96-103">RtlUTF8ToUnicodeN función)</span><span class="sxs-lookup"><span data-stu-id="64b96-103">RtlUTF8ToUnicodeN function</span></span>

<span data-ttu-id="64b96-104">Traduce la cadena de origen especificada en una cadena Unicode, usando la página de códigos del formato de transformación Unicode de 8 bits (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="64b96-104">Translates the specified source string into a Unicode string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b96-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64b96-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="64b96-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64b96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64b96-107">*UnicodeStringDestination* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="64b96-107">*UnicodeStringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64b96-108">Puntero a un búfer asignado por el llamador que recibe la cadena traducida.</span><span class="sxs-lookup"><span data-stu-id="64b96-108">A pointer to a caller-allocated buffer that receives the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="64b96-109">*UnicodeStringMaxByteCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64b96-109">*UnicodeStringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b96-110">Número máximo de bytes que se van a escribir en *UnicodeStringDestination*.</span><span class="sxs-lookup"><span data-stu-id="64b96-110">Maximum number of bytes to be written at *UnicodeStringDestination*.</span></span> <span data-ttu-id="64b96-111">Si este valor hace que la cadena traducida se trunque, **RtlUTF8ToUnicodeN** devuelve un estado de error.</span><span class="sxs-lookup"><span data-stu-id="64b96-111">If this value causes the translated string to be truncated, **RtlUTF8ToUnicodeN** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="64b96-112">*UnicodeStringActualByteCount* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="64b96-112">*UnicodeStringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="64b96-113">Puntero a una variable asignada por el llamador que recibe la longitud, en bytes, de la cadena traducida.</span><span class="sxs-lookup"><span data-stu-id="64b96-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="64b96-114">Este parámetro es opcional y puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="64b96-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="64b96-115">Si la cadena se trunca, el número devuelto cuenta el recuento de cadenas truncadas real.</span><span class="sxs-lookup"><span data-stu-id="64b96-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="64b96-116">*UTF8StringSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64b96-116">*UTF8StringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b96-117">Puntero a la cadena que se va a traducir.</span><span class="sxs-lookup"><span data-stu-id="64b96-117">A pointer to the string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="64b96-118">*UTF8StringByteCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64b96-118">*UTF8StringByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b96-119">Tamaño, en bytes, de la cadena en *UTF8StringSource*.</span><span class="sxs-lookup"><span data-stu-id="64b96-119">Size, in bytes, of the string at *UTF8StringSource*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64b96-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64b96-120">Return value</span></span>

<span data-ttu-id="64b96-121">**RtlUTF8ToUnicodeN** devuelve uno de los siguientes valores de NTSTATUS:</span><span class="sxs-lookup"><span data-stu-id="64b96-121">**RtlUTF8ToUnicodeN** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="64b96-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="64b96-122">Return code</span></span>                                                                                                  | <span data-ttu-id="64b96-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="64b96-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="64b96-124"><dt>**ESTADO \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="64b96-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="64b96-125">La cadena se convirtió a Unicode.</span><span class="sxs-lookup"><span data-stu-id="64b96-125">The string was converted to Unicode.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="64b96-126"><dt>**ESTADO \_ \_ no \_ asignado**</dt></span><span class="sxs-lookup"><span data-stu-id="64b96-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="64b96-127">Se encontró un carácter de entrada no válido y se ha reemplazado.</span><span class="sxs-lookup"><span data-stu-id="64b96-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="64b96-128">Este estado se considera un estado correcto.</span><span class="sxs-lookup"><span data-stu-id="64b96-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="64b96-129"><dt>**ESTADO \_ parámetro no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="64b96-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="64b96-130">Ambos punteros a *UnicodeStringDestination* y *UnicodeStringActualByteCount* eran **null**.</span><span class="sxs-lookup"><span data-stu-id="64b96-130">Both pointers to *UnicodeStringDestination* and *UnicodeStringActualByteCount* were **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="64b96-131"><dt>**Parámetro de estado \_ no válido \_ \_ 4**</dt></span><span class="sxs-lookup"><span data-stu-id="64b96-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="64b96-132">*UTF8StringSource* era **null**.</span><span class="sxs-lookup"><span data-stu-id="64b96-132">The *UTF8StringSource* was **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="64b96-133"><dt>**búfer de estado \_ \_ demasiado \_ pequeño**</dt></span><span class="sxs-lookup"><span data-stu-id="64b96-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="64b96-134">*UnicodeStringDestination* se truncó.</span><span class="sxs-lookup"><span data-stu-id="64b96-134">*UnicodeStringDestination* was truncated.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="64b96-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64b96-135">Remarks</span></span>

<span data-ttu-id="64b96-136">Aunque *UnicodeStringActualByteCount* es opcional y puede ser **null**, los llamadores deben proporcionar almacenamiento para él, ya que la longitud recibida se puede usar para determinar si la conversión se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="64b96-136">Although *UnicodeStringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span>

<span data-ttu-id="64b96-137">Si el resultado se trunca y se encuentra un carácter de entrada no válido, la función devuelve un error de búfer de estado \_ \_ demasiado \_ pequeño.</span><span class="sxs-lookup"><span data-stu-id="64b96-137">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="64b96-138">Si *UnicodeStringDestination* se establece en **null** , la función devolverá el número necesario de bytes para hospedar la cadena traducida sin ningún truncamiento en *UnicodeStringActualByteCount*.</span><span class="sxs-lookup"><span data-stu-id="64b96-138">If the *UnicodeStringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UnicodeStringActualByteCount*.</span></span>

<span data-ttu-id="64b96-139">**RtlUTF8ToUnicodeN** no modifica la cadena de origen a menos que los punteros *UnicodeStringDestination* y *UTF8StringSource* sean equivalentes.</span><span class="sxs-lookup"><span data-stu-id="64b96-139">**RtlUTF8ToUnicodeN** does not modify the source string unless the *UnicodeStringDestination* and *UTF8StringSource* pointers are equivalent.</span></span> <span data-ttu-id="64b96-140">La cadena Unicode devuelta no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="64b96-140">The returned Unicode string is not null-terminated.</span></span>

<span data-ttu-id="64b96-141">Los autores de llamadas de **RtlUTF8ToUnicodeN** deben ejecutarse en el nivel de distribución de IRQL < \_ .</span><span class="sxs-lookup"><span data-stu-id="64b96-141">Callers of **RtlUTF8ToUnicodeN** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="64b96-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64b96-142">Requirements</span></span>



| <span data-ttu-id="64b96-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="64b96-143">Requirement</span></span> | <span data-ttu-id="64b96-144">Value</span><span class="sxs-lookup"><span data-stu-id="64b96-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="64b96-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64b96-145">Minimum supported client</span></span><br/> | <span data-ttu-id="64b96-146">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="64b96-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="64b96-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64b96-147">Minimum supported server</span></span><br/> | <span data-ttu-id="64b96-148">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="64b96-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="64b96-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64b96-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="64b96-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="64b96-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="64b96-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64b96-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64b96-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64b96-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b96-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="64b96-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b96-154">**RtlUnicodeToUTF8N**</span><span class="sxs-lookup"><span data-stu-id="64b96-154">**RtlUnicodeToUTF8N**</span></span>](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




