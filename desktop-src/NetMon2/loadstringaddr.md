---
description: La función LoadStringAddr transforma una cadena (como &\# 0034; 157.54.32.45&\# 0034;) y crea una dirección DWORD.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: Función LoadStringAddr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677414"
---
# <a name="loadstringaddr-function"></a><span data-ttu-id="df0c6-103">LoadStringAddr función)</span><span class="sxs-lookup"><span data-stu-id="df0c6-103">LoadStringAddr function</span></span>

<span data-ttu-id="df0c6-104">La función **LoadStringAddr** transforma una cadena (por ejemplo, "157.54.32.45") y crea una dirección **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="df0c6-104">The **LoadStringAddr** function transforms a string (such as "157.54.32.45") and creates a **DWORD** address.</span></span>

## <a name="syntax"></a><span data-ttu-id="df0c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df0c6-105">Syntax</span></span>


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a><span data-ttu-id="df0c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df0c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df0c6-107">*pAddress*</span><span class="sxs-lookup"><span data-stu-id="df0c6-107">*pAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="df0c6-108">Puntero a un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="df0c6-108">Pointer to a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="df0c6-109">*str*</span><span class="sxs-lookup"><span data-stu-id="df0c6-109">*str*</span></span> 
</dt> <dd>

<span data-ttu-id="df0c6-110">Puntero a una cadena de caracteres con la representación x. x. x. x de una dirección IP (por ejemplo, 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="df0c6-110">Pointer to a character string with x.x.x.x representation of an IP address (for example,127.0.0.1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df0c6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df0c6-111">Return value</span></span>

<span data-ttu-id="df0c6-112">Si la función es correcta (se encontró el nombre de la dirección); el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="df0c6-112">If the function is successful (the address name was found); the return value is **TRUE**.</span></span>

<span data-ttu-id="df0c6-113">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="df0c6-113">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="df0c6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df0c6-114">Requirements</span></span>



| <span data-ttu-id="df0c6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="df0c6-115">Requirement</span></span> | <span data-ttu-id="df0c6-116">Value</span><span class="sxs-lookup"><span data-stu-id="df0c6-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="df0c6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df0c6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="df0c6-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="df0c6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="df0c6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df0c6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="df0c6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="df0c6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="df0c6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df0c6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="df0c6-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="df0c6-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="df0c6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df0c6-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="df0c6-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df0c6-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="df0c6-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df0c6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df0c6-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df0c6-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




