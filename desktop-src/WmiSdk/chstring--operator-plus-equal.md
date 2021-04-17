---
description: El operador de concatenación + = une los caracteres al final de esta cadena. El operador acepta otro objeto CHString, un puntero de carácter o un carácter único.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'CHString:: Operator + = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716211"
---
# <a name="chstringoperator"></a><span data-ttu-id="45d54-104">CHString:: Operator + =</span><span class="sxs-lookup"><span data-stu-id="45d54-104">CHString::operator+=</span></span>

<span data-ttu-id="45d54-105">\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="45d54-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="45d54-106">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="45d54-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="45d54-107">El operador de concatenación + = une los caracteres al final de esta cadena.</span><span class="sxs-lookup"><span data-stu-id="45d54-107">The += concatenation operator joins characters to the end of this string.</span></span> <span data-ttu-id="45d54-108">El operador acepta otro objeto [**CHString**](chstring.md) , un puntero de carácter o un carácter único.</span><span class="sxs-lookup"><span data-stu-id="45d54-108">The operator accepts another [**CHString**](chstring.md) object, a character pointer, or a single character.</span></span>

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="45d54-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45d54-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45d54-110"><span id="string"></span><span id="STRING"></span>*String@*</span><span class="sxs-lookup"><span data-stu-id="45d54-110"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="45d54-111">Una cadena [**CHString**](chstring.md) que se concatena con esta cadena.</span><span class="sxs-lookup"><span data-stu-id="45d54-111">A [**CHString**](chstring.md) string that concatenates to this string.</span></span>

</dd> <dt>

<span data-ttu-id="45d54-112"><span id="ch"></span><span id="CH"></span>*Cam*</span><span class="sxs-lookup"><span data-stu-id="45d54-112"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="45d54-113">Carácter que se va a concatenar con esta cadena.</span><span class="sxs-lookup"><span data-stu-id="45d54-113">A character to concatenate to this string.</span></span>

</dd> <dt>

<span data-ttu-id="45d54-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="45d54-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="45d54-115">Puntero a una cadena terminada en **null** que se va a concatenar con esta cadena.</span><span class="sxs-lookup"><span data-stu-id="45d54-115">Pointer to a **NULL**-terminated string to concatenate to this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45d54-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45d54-116">Remarks</span></span>

<span data-ttu-id="45d54-117">Tenga en cuenta que se pueden producir excepciones de memoria cada vez que utilice este operador de concatenación porque se puede asignar un nuevo almacenamiento para los caracteres agregados a este objeto [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="45d54-117">Be aware that memory exceptions can occur whenever you use this concatenation operator because new storage may be allocated for characters added to this [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="45d54-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="45d54-118">Examples</span></span>

<span data-ttu-id="45d54-119">En el ejemplo siguiente se muestra el uso de **CHString:: Operator + =**:</span><span class="sxs-lookup"><span data-stu-id="45d54-119">The following example shows the use of **CHString::operator +=**:</span></span>


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a><span data-ttu-id="45d54-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45d54-120">Requirements</span></span>



| <span data-ttu-id="45d54-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="45d54-121">Requirement</span></span> | <span data-ttu-id="45d54-122">Value</span><span class="sxs-lookup"><span data-stu-id="45d54-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d54-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45d54-123">Minimum supported client</span></span><br/> | <span data-ttu-id="45d54-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45d54-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="45d54-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45d54-125">Minimum supported server</span></span><br/> | <span data-ttu-id="45d54-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45d54-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="45d54-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45d54-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="45d54-128"><dt>ChString. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45d54-128"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="45d54-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45d54-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="45d54-130"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45d54-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="45d54-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45d54-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45d54-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45d54-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d54-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="45d54-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d54-134">**CHString**</span><span class="sxs-lookup"><span data-stu-id="45d54-134">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

