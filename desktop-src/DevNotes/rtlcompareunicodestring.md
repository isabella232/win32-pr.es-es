---
description: Compara dos cadenas Unicode.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Función RtlCompareUnicodeString (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907194"
---
# <a name="rtlcompareunicodestring-function"></a><span data-ttu-id="549ea-103">RtlCompareUnicodeString función)</span><span class="sxs-lookup"><span data-stu-id="549ea-103">RtlCompareUnicodeString function</span></span>

<span data-ttu-id="549ea-104">Compara dos cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="549ea-104">Compares two Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="549ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="549ea-105">Syntax</span></span>


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="549ea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="549ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="549ea-107">*Cadena1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="549ea-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="549ea-108">Puntero a la primera cadena.</span><span class="sxs-lookup"><span data-stu-id="549ea-108">Pointer to the first string.</span></span>

</dd> <dt>

<span data-ttu-id="549ea-109">*Cadena2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="549ea-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="549ea-110">Puntero a la segunda cadena.</span><span class="sxs-lookup"><span data-stu-id="549ea-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="549ea-111">*CaseInSensitive* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="549ea-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="549ea-112">Si **es true**, se debe pasar por alto la distinción de mayúsculas y minúsculas al realizar la comparación.</span><span class="sxs-lookup"><span data-stu-id="549ea-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="549ea-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="549ea-113">Return value</span></span>

<span data-ttu-id="549ea-114">Valor con signo que proporciona los resultados de la comparación:</span><span class="sxs-lookup"><span data-stu-id="549ea-114">A signed value that gives the results of the comparison:</span></span>



| <span data-ttu-id="549ea-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="549ea-115">Return code</span></span>                                                                               | <span data-ttu-id="549ea-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="549ea-116">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="549ea-117"><dt>**Nulo**</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-117"><dt>**Zero**</dt></span></span> </dl>       | <span data-ttu-id="549ea-118">*String1* es igual a *cadena2*.</span><span class="sxs-lookup"><span data-stu-id="549ea-118">*String1* equals *String2*.</span></span><br/>          |
| <dl> <span data-ttu-id="549ea-119"><dt>**< cero**</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-119"><dt>**< Zero**</dt></span></span> </dl>  | <span data-ttu-id="549ea-120">*String1* es menor que *cadena2*.</span><span class="sxs-lookup"><span data-stu-id="549ea-120">*String1* is less than *String2*.</span></span><br/>    |
| <dl> <span data-ttu-id="549ea-121"><dt>**> cero**</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-121"><dt>**> Zero** </dt></span></span> </dl> | <span data-ttu-id="549ea-122">*String1* es mayor que *cadena2*.</span><span class="sxs-lookup"><span data-stu-id="549ea-122">*String1* is greater than *String2*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="549ea-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="549ea-123">Requirements</span></span>



| <span data-ttu-id="549ea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="549ea-124">Requirement</span></span> | <span data-ttu-id="549ea-125">Value</span><span class="sxs-lookup"><span data-stu-id="549ea-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="549ea-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="549ea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="549ea-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="549ea-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="549ea-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="549ea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="549ea-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="549ea-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="549ea-130">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="549ea-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="549ea-131"><dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="549ea-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="549ea-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="549ea-133"><dt>WDM. h (incluir WDM. h, Ntddk. h o Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-133"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="549ea-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="549ea-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="549ea-135"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="549ea-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="549ea-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="549ea-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="549ea-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="549ea-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="549ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="549ea-139">**RtlCompareString**</span><span class="sxs-lookup"><span data-stu-id="549ea-139">**RtlCompareString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[<span data-ttu-id="549ea-140">**RtlEqualString**</span><span class="sxs-lookup"><span data-stu-id="549ea-140">**RtlEqualString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
