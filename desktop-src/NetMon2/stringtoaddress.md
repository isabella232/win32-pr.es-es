---
description: La función StringToAddress convierte una cadena en una dirección.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Función StringToAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687318"
---
# <a name="stringtoaddress-function"></a><span data-ttu-id="f7cab-103">StringToAddress función)</span><span class="sxs-lookup"><span data-stu-id="f7cab-103">StringToAddress function</span></span>

<span data-ttu-id="f7cab-104">La función **StringToAddress** convierte una cadena en una dirección.</span><span class="sxs-lookup"><span data-stu-id="f7cab-104">The **StringToAddress** function converts a string to an address.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7cab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7cab-105">Syntax</span></span>


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a><span data-ttu-id="f7cab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7cab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7cab-107">*lpAddress* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f7cab-107">*lpAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7cab-108">Puntero a la dirección a la que se convierte la cadena.</span><span class="sxs-lookup"><span data-stu-id="f7cab-108">Pointer to the address the string is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="f7cab-109">*cadena* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f7cab-109">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7cab-110">Cadena que se convierte en una dirección.</span><span class="sxs-lookup"><span data-stu-id="f7cab-110">String that is converted to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7cab-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7cab-111">Return value</span></span>

<span data-ttu-id="f7cab-112">El valor devuelto es un puntero a la cadena convertida.</span><span class="sxs-lookup"><span data-stu-id="f7cab-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7cab-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7cab-113">Requirements</span></span>



| <span data-ttu-id="f7cab-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7cab-114">Requirement</span></span> | <span data-ttu-id="f7cab-115">Value</span><span class="sxs-lookup"><span data-stu-id="f7cab-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7cab-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7cab-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f7cab-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f7cab-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f7cab-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7cab-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f7cab-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7cab-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7cab-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7cab-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7cab-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7cab-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7cab-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7cab-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7cab-123"><dt>Analizador. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7cab-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7cab-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f7cab-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7cab-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7cab-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




