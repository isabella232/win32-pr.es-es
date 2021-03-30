---
description: El operador de concatenación + combina dos cadenas y devuelve un objeto CHString.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'CHString:: Operator + (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815982"
---
# <a name="chstringoperator"></a><span data-ttu-id="01647-103">CHString:: Operator +</span><span class="sxs-lookup"><span data-stu-id="01647-103">CHString::operator+</span></span>

<span data-ttu-id="01647-104">\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="01647-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="01647-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="01647-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="01647-106">El operador de concatenación + combina dos cadenas y devuelve un objeto [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="01647-106">The + concatenation operator joins two strings and returns a [**CHString**](chstring.md) object.</span></span>

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="01647-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01647-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01647-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*Str, Str1, str2*</span><span class="sxs-lookup"><span data-stu-id="01647-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*</span></span>
</dt> <dd>

<span data-ttu-id="01647-109">Cadenas [**CHString**](chstring.md) que se concatenan.</span><span class="sxs-lookup"><span data-stu-id="01647-109">[**CHString**](chstring.md) strings that are concatenated.</span></span>

</dd> <dt>

<span data-ttu-id="01647-110"><span id="ch"></span><span id="CH"></span>*Cam*</span><span class="sxs-lookup"><span data-stu-id="01647-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="01647-111">Carácter que se concatena con una cadena o una cadena que se concatena con un carácter.</span><span class="sxs-lookup"><span data-stu-id="01647-111">A character that concatenates to a string or a string that concatenates to a character.</span></span>

</dd> <dt>

<span data-ttu-id="01647-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="01647-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="01647-113">Puntero a una cadena de caracteres terminada en **null**.</span><span class="sxs-lookup"><span data-stu-id="01647-113">Pointer to a **NULL**-terminated character string.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="01647-114">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="01647-114">Return Values</span></span>

<span data-ttu-id="01647-115">Este operador de concatenación devuelve un objeto [**CHString**](chstring.md) que es el resultado temporal de la concatenación.</span><span class="sxs-lookup"><span data-stu-id="01647-115">This concatenation operator returns a [**CHString**](chstring.md) object that is the temporary result of the concatenation.</span></span> <span data-ttu-id="01647-116">Este valor devuelto permite combinar varias concatenaciones en la misma expresión.</span><span class="sxs-lookup"><span data-stu-id="01647-116">This return value makes it possible to combine several concatenations in the same expression.</span></span>

## <a name="remarks"></a><span data-ttu-id="01647-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01647-117">Remarks</span></span>

<span data-ttu-id="01647-118">Una de las dos cadenas de argumentos debe ser un objeto [**CHString**](chstring.md) ; el otro puede ser un puntero de carácter o un carácter.</span><span class="sxs-lookup"><span data-stu-id="01647-118">One of the two argument strings must be a [**CHString**](chstring.md) object; the other can be a character pointer or a character.</span></span> <span data-ttu-id="01647-119">Tenga en cuenta que pueden producirse excepciones de memoria cada vez que se usa el operador de concatenación, ya que se puede asignar un nuevo almacenamiento para almacenar datos temporales.</span><span class="sxs-lookup"><span data-stu-id="01647-119">Be aware that memory exceptions can occur whenever you use the concatenation operator because new storage may be allocated to hold temporary data.</span></span>

## <a name="examples"></a><span data-ttu-id="01647-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="01647-120">Examples</span></span>

<span data-ttu-id="01647-121">En el ejemplo de código siguiente se muestra el uso de **CHString:: Operator +**:</span><span class="sxs-lookup"><span data-stu-id="01647-121">The following code example shows the use of **CHString::operator +**:</span></span>


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
```



## <a name="requirements"></a><span data-ttu-id="01647-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01647-122">Requirements</span></span>



| <span data-ttu-id="01647-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="01647-123">Requirement</span></span> | <span data-ttu-id="01647-124">Value</span><span class="sxs-lookup"><span data-stu-id="01647-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01647-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01647-125">Minimum supported client</span></span><br/> | <span data-ttu-id="01647-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01647-126">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="01647-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01647-127">Minimum supported server</span></span><br/> | <span data-ttu-id="01647-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01647-128">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="01647-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01647-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="01647-130"><dt>ChString. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01647-130"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="01647-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01647-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="01647-132"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01647-132"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="01647-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01647-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01647-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01647-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01647-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="01647-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01647-136">**CHString**</span><span class="sxs-lookup"><span data-stu-id="01647-136">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

