---
description: Calcula el hash final de los datos especificados por la función MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: Función A_SHAFinal (Sha. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670396"
---
# <a name="a_shafinal-function"></a><span data-ttu-id="cd5d8-103">Una \_ función SHAFinal</span><span class="sxs-lookup"><span data-stu-id="cd5d8-103">A\_SHAFinal function</span></span>

<span data-ttu-id="cd5d8-104">Calcula el hash final de los datos especificados por la función MD5Update.</span><span class="sxs-lookup"><span data-stu-id="cd5d8-104">Computes the final hash of the data entered by the MD5Update function.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd5d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd5d8-105">Syntax</span></span>


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a><span data-ttu-id="cd5d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd5d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd5d8-107">*Contexto* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="cd5d8-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd5d8-108">Contexto SHA.</span><span class="sxs-lookup"><span data-stu-id="cd5d8-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="cd5d8-109">*Resultado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cd5d8-109">*Result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd5d8-110">Tabla hash resultante.</span><span class="sxs-lookup"><span data-stu-id="cd5d8-110">The resulting hash table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd5d8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd5d8-111">Return value</span></span>

<span data-ttu-id="cd5d8-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cd5d8-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd5d8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd5d8-113">Remarks</span></span>

<span data-ttu-id="cd5d8-114">Esta función es muy similar a SHAFinal, pero se llama directamente desde la biblioteca, en lugar de enrutarse a través de la infraestructura de criptografía.</span><span class="sxs-lookup"><span data-stu-id="cd5d8-114">This function is very similar to SHAFinal, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="cd5d8-115">Para obtener más información, consulte [proveedores de Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="cd5d8-115">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd5d8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd5d8-116">Requirements</span></span>



| <span data-ttu-id="cd5d8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd5d8-117">Requirement</span></span> | <span data-ttu-id="cd5d8-118">Value</span><span class="sxs-lookup"><span data-stu-id="cd5d8-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd5d8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd5d8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cd5d8-120"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd5d8-120"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="cd5d8-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd5d8-121">Library</span></span><br/> | <dl> <span data-ttu-id="cd5d8-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd5d8-122"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="cd5d8-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd5d8-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="cd5d8-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd5d8-124"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
