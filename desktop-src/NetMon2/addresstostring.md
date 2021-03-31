---
description: La función AddressToString convierte una dirección en una cadena.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Función AddressToString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156841"
---
# <a name="addresstostring-function"></a><span data-ttu-id="320ea-103">AddressToString función)</span><span class="sxs-lookup"><span data-stu-id="320ea-103">AddressToString function</span></span>

<span data-ttu-id="320ea-104">La función **AddressToString** convierte una dirección en una cadena.</span><span class="sxs-lookup"><span data-stu-id="320ea-104">The **AddressToString** function converts an address into a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="320ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="320ea-105">Syntax</span></span>


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="320ea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="320ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="320ea-107">*cadena* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="320ea-107">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="320ea-108">Cadena a la que se convierte la dirección.</span><span class="sxs-lookup"><span data-stu-id="320ea-108">String that the address is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="320ea-109">*lpAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="320ea-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="320ea-110">Dirección que se imprime.</span><span class="sxs-lookup"><span data-stu-id="320ea-110">The address that is printed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="320ea-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="320ea-111">Return value</span></span>

<span data-ttu-id="320ea-112">El valor devuelto es un puntero a la cadena convertida.</span><span class="sxs-lookup"><span data-stu-id="320ea-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="320ea-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="320ea-113">Requirements</span></span>



| <span data-ttu-id="320ea-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="320ea-114">Requirement</span></span> | <span data-ttu-id="320ea-115">Value</span><span class="sxs-lookup"><span data-stu-id="320ea-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="320ea-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="320ea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="320ea-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="320ea-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="320ea-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="320ea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="320ea-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="320ea-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="320ea-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="320ea-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="320ea-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="320ea-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="320ea-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="320ea-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="320ea-123"><dt>Analizador. lib</dt></span><span class="sxs-lookup"><span data-stu-id="320ea-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="320ea-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="320ea-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="320ea-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="320ea-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




