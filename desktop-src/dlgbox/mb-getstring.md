---
title: MB_GetString función (User. h)
description: Devuelve cadenas para los botones de cuadro de mensaje estándar.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- MB_GetString cuadros de diálogo de función
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700102"
---
# <a name="mb_getstring-function"></a><span data-ttu-id="3b4fd-104">MB \_ GetString (función)</span><span class="sxs-lookup"><span data-stu-id="3b4fd-104">MB\_GetString function</span></span>

<span data-ttu-id="3b4fd-105">Devuelve cadenas para los botones de cuadro de mensaje estándar.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-105">Returns strings for standard message box buttons.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b4fd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b4fd-106">Syntax</span></span>


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a><span data-ttu-id="3b4fd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b4fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b4fd-108">*wBtn*</span><span class="sxs-lookup"><span data-stu-id="3b4fd-108">*wBtn*</span></span> 
</dt> <dd>

<span data-ttu-id="3b4fd-109">Identificador de la cadena que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-109">The id of the string to return.</span></span> <span data-ttu-id="3b4fd-110">Se identifican mediante los valores de identificador de comando del cuadro de diálogo enumerados en Winuser. h.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-110">These are identified by the Dialog Box Command ID values listed in winuser.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b4fd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b4fd-111">Return value</span></span>

<span data-ttu-id="3b4fd-112">La cadena o NULL si no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-112">The string, or NULL if not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b4fd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b4fd-113">Requirements</span></span>



| <span data-ttu-id="3b4fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b4fd-114">Requirement</span></span> | <span data-ttu-id="3b4fd-115">Value</span><span class="sxs-lookup"><span data-stu-id="3b4fd-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b4fd-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b4fd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3b4fd-117"><dt>User. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b4fd-117"><dt>User.h</dt></span></span> </dl>     |
| <span data-ttu-id="3b4fd-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b4fd-118">Library</span></span><br/> | <dl> <span data-ttu-id="3b4fd-119"><dt>User32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b4fd-119"><dt>User32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3b4fd-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b4fd-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b4fd-121"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b4fd-121"><dt>User32.dll</dt></span></span> </dl> |



 

 





