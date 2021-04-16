---
description: Inicia el hash de un flujo de datos.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: Función A_SHAInit (Sha. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689990"
---
# <a name="a_shainit-function"></a><span data-ttu-id="caac7-103">Una \_ función SHAInit</span><span class="sxs-lookup"><span data-stu-id="caac7-103">A\_SHAInit function</span></span>

<span data-ttu-id="caac7-104">Inicia el hash de un flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="caac7-104">Initiates the hashing of a stream of data.</span></span>

## <a name="syntax"></a><span data-ttu-id="caac7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="caac7-105">Syntax</span></span>


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a><span data-ttu-id="caac7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="caac7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caac7-107">*Contexto* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="caac7-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="caac7-108">Contexto SHA.</span><span class="sxs-lookup"><span data-stu-id="caac7-108">The SHA context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caac7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="caac7-109">Return value</span></span>

<span data-ttu-id="caac7-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="caac7-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="caac7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="caac7-111">Remarks</span></span>

<span data-ttu-id="caac7-112">Esta función es muy similar a SHAInit, pero se llama directamente desde la biblioteca, en lugar de enrutarse a través de la infraestructura de criptografía.</span><span class="sxs-lookup"><span data-stu-id="caac7-112">This function is very similar to SHAInit, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="caac7-113">Para obtener más información, consulte [proveedores de Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="caac7-113">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="caac7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="caac7-114">Requirements</span></span>



| <span data-ttu-id="caac7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="caac7-115">Requirement</span></span> | <span data-ttu-id="caac7-116">Value</span><span class="sxs-lookup"><span data-stu-id="caac7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="caac7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="caac7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="caac7-118"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="caac7-118"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="caac7-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="caac7-119">Library</span></span><br/> | <dl> <span data-ttu-id="caac7-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caac7-120"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="caac7-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="caac7-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="caac7-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caac7-122"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
