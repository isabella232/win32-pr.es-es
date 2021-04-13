---
description: Compara dos cadenas Unicode para determinar si una cadena es un prefijo del otro.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Función RtlPrefixUnicodeString (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496103"
---
# <a name="rtlprefixunicodestring-function"></a><span data-ttu-id="cc3ce-103">RtlPrefixUnicodeString función)</span><span class="sxs-lookup"><span data-stu-id="cc3ce-103">RtlPrefixUnicodeString function</span></span>

<span data-ttu-id="cc3ce-104">Compara dos cadenas Unicode para determinar si una cadena es un prefijo del otro.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-104">Compares two Unicode strings to determine whether one string is a prefix of the other.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc3ce-105">Syntax</span></span>


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="cc3ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc3ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc3ce-107">*Cadena1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc3ce-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3ce-108">Puntero a la primera cadena, que puede ser un prefijo de la cadena Unicode almacenada en el búfer en *cadena2*.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-108">Pointer to the first string, which might be a prefix of the buffered Unicode string at *String2*.</span></span>

</dd> <dt>

<span data-ttu-id="cc3ce-109">*Cadena2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc3ce-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3ce-110">Puntero a la segunda cadena.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="cc3ce-111">*CaseInSensitive* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc3ce-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3ce-112">Si **es true**, se debe pasar por alto la distinción de mayúsculas y minúsculas al realizar la comparación.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc3ce-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc3ce-113">Return value</span></span>

<span data-ttu-id="cc3ce-114">**True** si *string1* es un prefijo de *cadena2*.</span><span class="sxs-lookup"><span data-stu-id="cc3ce-114">**TRUE** if *String1* is a prefix of *String2*.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc3ce-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc3ce-115">Requirements</span></span>



| <span data-ttu-id="cc3ce-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc3ce-116">Requirement</span></span> | <span data-ttu-id="cc3ce-117">Value</span><span class="sxs-lookup"><span data-stu-id="cc3ce-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3ce-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc3ce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cc3ce-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cc3ce-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="cc3ce-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc3ce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cc3ce-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc3ce-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="cc3ce-122">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="cc3ce-122">Target platform</span></span><br/>          | <dl> <span data-ttu-id="cc3ce-123"><dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="cc3ce-123"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="cc3ce-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc3ce-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc3ce-125"><dt>Ntddk. h (incluye Ntddk. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc3ce-125"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="cc3ce-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc3ce-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc3ce-127"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc3ce-127"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cc3ce-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc3ce-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc3ce-129"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc3ce-129"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="cc3ce-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc3ce-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc3ce-131">**RtlCompareUnicodeString**</span><span class="sxs-lookup"><span data-stu-id="cc3ce-131">**RtlCompareUnicodeString**</span></span>](rtlcompareunicodestring.md)
</dt> </dl>

 

 




