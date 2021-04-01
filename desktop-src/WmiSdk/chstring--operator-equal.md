---
description: El operador de asignación CHString (=) reinicializa un objeto CHString existente con nuevos datos.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'CHString:: Operator = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9abfa9ea2b72aa8f6830d9fb6388861c8c3b82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082758"
---
# <a name="chstringoperator"></a><span data-ttu-id="85811-103">CHString:: Operator =</span><span class="sxs-lookup"><span data-stu-id="85811-103">CHString::operator=</span></span>

<span data-ttu-id="85811-104">\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="85811-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="85811-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="85811-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="85811-106">El operador de asignación [**CHString**](chstring.md) (=) reinicializa un objeto CHString existente con nuevos datos.</span><span class="sxs-lookup"><span data-stu-id="85811-106">The [**CHString**](chstring.md) assignment (=) operator reinitializes an existing CHString object with new data.</span></span>

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="85811-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85811-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85811-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span><span class="sxs-lookup"><span data-stu-id="85811-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span></span>
</dt> <dd>

<span data-ttu-id="85811-109">Asigna una cadena [**CHString**](chstring.md) a este objeto.</span><span class="sxs-lookup"><span data-stu-id="85811-109">Assigns a [**CHString**](chstring.md) string to this object.</span></span>

</dd> <dt>

<span data-ttu-id="85811-110"><span id="ch"></span><span id="CH"></span>*Cam*</span><span class="sxs-lookup"><span data-stu-id="85811-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="85811-111">Asigna un carácter a este objeto.</span><span class="sxs-lookup"><span data-stu-id="85811-111">Assigns a character to this object.</span></span>

</dd> <dt>

<span data-ttu-id="85811-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *PSZ*</span><span class="sxs-lookup"><span data-stu-id="85811-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*</span></span>
</dt> <dd>

<span data-ttu-id="85811-113">Asigna una cadena terminada en **null** a este objeto.</span><span class="sxs-lookup"><span data-stu-id="85811-113">Assigns a **NULL**-terminated string to this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85811-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85811-114">Remarks</span></span>

<span data-ttu-id="85811-115">Si la cadena de destino (es decir, el lado izquierdo) ya es lo suficientemente grande como para almacenar los datos nuevos, no se realiza ninguna asignación de memoria nueva.</span><span class="sxs-lookup"><span data-stu-id="85811-115">If the destination string (that is, the left side) is already large enough to store the new data, no new memory allocation is performed.</span></span> <span data-ttu-id="85811-116">Sin embargo, pueden producirse excepciones de memoria cada vez que se usa el operador de asignación porque a menudo se asigna un nuevo almacenamiento para contener el objeto [**CHString**](chstring.md) resultante.</span><span class="sxs-lookup"><span data-stu-id="85811-116">However, memory exceptions can occur whenever you use the assignment operator because new storage is often allocated to hold the resulting [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="85811-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="85811-117">Examples</span></span>

<span data-ttu-id="85811-118">En el ejemplo de código siguiente se muestra el uso de **CHString:: Operator =**:</span><span class="sxs-lookup"><span data-stu-id="85811-118">The following code example shows the use of **CHString::operator =**:</span></span>


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a><span data-ttu-id="85811-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85811-119">Requirements</span></span>



| <span data-ttu-id="85811-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="85811-120">Requirement</span></span> | <span data-ttu-id="85811-121">Value</span><span class="sxs-lookup"><span data-stu-id="85811-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85811-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85811-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85811-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85811-123">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="85811-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85811-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85811-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85811-125">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="85811-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85811-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="85811-127"><dt>ChString. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85811-127"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="85811-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85811-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="85811-129"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85811-129"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="85811-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85811-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85811-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85811-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85811-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="85811-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85811-133">**CHString**</span><span class="sxs-lookup"><span data-stu-id="85811-133">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

