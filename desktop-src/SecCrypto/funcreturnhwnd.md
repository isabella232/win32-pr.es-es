---
description: Lo utiliza un proveedor de servicios criptográficos (CSP) para obtener el identificador de ventana que el CSP debe utilizar como elemento primario o propietario de cualquier interfaz de usuario que se muestre.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: CRYPT_RETURN_HWND puntero a función (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669667"
---
# <a name="crypt_return_hwnd-function-pointer"></a><span data-ttu-id="37832-103">CRYPT \_ Return ( \_ puntero de función HWND)</span><span class="sxs-lookup"><span data-stu-id="37832-103">CRYPT\_RETURN\_HWND function pointer</span></span>

<span data-ttu-id="37832-104">Un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) utiliza la función de devolución de llamada **FuncReturnhWnd** para obtener el identificador de ventana que el CSP debe usar como elemento primario o propietario de cualquier interfaz de usuario que se muestra.</span><span class="sxs-lookup"><span data-stu-id="37832-104">The **FuncReturnhWnd** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to obtain the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="37832-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37832-105">Syntax</span></span>


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a><span data-ttu-id="37832-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37832-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37832-107">*phWnd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37832-107">*phWnd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37832-108">Dirección de una variable **hWnd** que recibe el identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="37832-108">The address of an **HWND** variable that receives the parent window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37832-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37832-109">Return value</span></span>

<span data-ttu-id="37832-110">Este puntero de función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="37832-110">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="37832-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37832-111">Requirements</span></span>



| <span data-ttu-id="37832-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="37832-112">Requirement</span></span> | <span data-ttu-id="37832-113">Value</span><span class="sxs-lookup"><span data-stu-id="37832-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37832-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37832-114">Minimum supported client</span></span><br/> | <span data-ttu-id="37832-115">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="37832-115">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37832-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37832-116">Minimum supported server</span></span><br/> | <span data-ttu-id="37832-117">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="37832-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="37832-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37832-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="37832-119"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="37832-119"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37832-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="37832-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37832-121">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="37832-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="37832-122">**VTableProvStruc**</span><span class="sxs-lookup"><span data-stu-id="37832-122">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
