---
description: Estos operadores de subíndice establecen u obtienen el elemento en el índice especificado. Estos operadores son un sustituto práctico de los métodos SetAt y GetAd.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'CHStringArray:: Operator [] (ChStrArr. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716767"
---
# <a name="chstringarrayoperator--"></a><span data-ttu-id="c3650-104">CHStringArray:: Operator \[\]</span><span class="sxs-lookup"><span data-stu-id="c3650-104">CHStringArray::operator \[ \]</span></span>

<span data-ttu-id="c3650-105">\[La clase [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="c3650-105">\[The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="c3650-106">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="c3650-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="c3650-107">Estos operadores de subíndice establecen u obtienen el elemento en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c3650-107">These subscript operators set or get the element at the specified index.</span></span> <span data-ttu-id="c3650-108">Estos operadores son un sustituto práctico de los métodos [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) y [**GetAd**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) .</span><span class="sxs-lookup"><span data-stu-id="c3650-108">These operators are a convenient substitute for the [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) and [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) methods.</span></span>

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a><span data-ttu-id="c3650-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3650-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3650-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span><span class="sxs-lookup"><span data-stu-id="c3650-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span></span>
</dt> <dd>

<span data-ttu-id="c3650-111">Índice entero que es mayor o igual que cero y menor o igual que el valor devuelto por [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span><span class="sxs-lookup"><span data-stu-id="c3650-111">An integer index that is greater than or equal to zero and less than or equal to the value returned by [**GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="c3650-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c3650-112">Return Values</span></span>

<span data-ttu-id="c3650-113">Los operadores de subíndice devuelven el elemento de puntero [**CHString**](chstring.md) actualmente en este índice.</span><span class="sxs-lookup"><span data-stu-id="c3650-113">The subscript operators return the [**CHString**](chstring.md) pointer element currently at this index.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3650-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3650-114">Remarks</span></span>

<span data-ttu-id="c3650-115">Puede usar el primer operador, que llama a las matrices que no son **const**, tanto en la parte derecha (r-value) como en el lado izquierdo (valor l) de una instrucción de asignación.</span><span class="sxs-lookup"><span data-stu-id="c3650-115">You can use the first operator, which calls for arrays that are not **const**, on either the right (r-value) or the left (l-value) side of an assignment statement.</span></span> <span data-ttu-id="c3650-116">La segunda, que llama a las matrices **const** , solo se puede usar a la derecha.</span><span class="sxs-lookup"><span data-stu-id="c3650-116">The second, which calls for **const** arrays, can be used only on the right.</span></span>

<span data-ttu-id="c3650-117">La versión de depuración de la biblioteca valida si el subíndice (ya sea en el lado izquierdo o derecho de una instrucción de asignación) está fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="c3650-117">The debug version of the library asserts if the subscript (either on the left or right side of an assignment statement) is out of bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="c3650-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c3650-118">Examples</span></span>

<span data-ttu-id="c3650-119">En el ejemplo de código siguiente se muestra el uso de [**CHStringArray \[ \] :: Operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c3650-119">The following code example shows the use of [**CHStringArray::operator \[\]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span></span>


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a><span data-ttu-id="c3650-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3650-120">Requirements</span></span>



| <span data-ttu-id="c3650-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3650-121">Requirement</span></span> | <span data-ttu-id="c3650-122">Value</span><span class="sxs-lookup"><span data-stu-id="c3650-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3650-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3650-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c3650-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3650-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="c3650-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3650-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c3650-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3650-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="c3650-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3650-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3650-128"><dt>ChStrArr. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3650-128"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c3650-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3650-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c3650-130"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3650-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="c3650-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3650-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3650-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3650-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3650-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3650-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3650-134">**CHStringArray:: Add**</span><span class="sxs-lookup"><span data-stu-id="c3650-134">**CHStringArray::Add**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

<span data-ttu-id="c3650-135">[**CHStringArray:: GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span><span class="sxs-lookup"><span data-stu-id="c3650-135">[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span></span>
</dt> <dt>

<span data-ttu-id="c3650-136">[**CHStringArray:: SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="c3650-136">[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span></span>
</dt> </dl>

