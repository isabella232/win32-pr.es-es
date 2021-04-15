---
description: Agrega datos a un objeto hash especificado.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: Función A_SHAUpdate (Sha. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689989"
---
# <a name="a_shaupdate-function"></a><span data-ttu-id="48a21-103">Una \_ función SHAUpdate</span><span class="sxs-lookup"><span data-stu-id="48a21-103">A\_SHAUpdate function</span></span>

<span data-ttu-id="48a21-104">Agrega datos a un objeto hash especificado.</span><span class="sxs-lookup"><span data-stu-id="48a21-104">Adds data to a specified hash object.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a21-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48a21-105">Syntax</span></span>


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="48a21-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48a21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a21-107">*Contexto* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="48a21-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="48a21-108">Contexto SHA.</span><span class="sxs-lookup"><span data-stu-id="48a21-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="48a21-109">*Búfer* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="48a21-109">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48a21-110">Tabla hash.</span><span class="sxs-lookup"><span data-stu-id="48a21-110">The hash table.</span></span>

</dd> <dt>

<span data-ttu-id="48a21-111">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="48a21-111">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="48a21-112">Tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="48a21-112">The size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a21-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48a21-113">Return value</span></span>

<span data-ttu-id="48a21-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="48a21-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48a21-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48a21-115">Remarks</span></span>

<span data-ttu-id="48a21-116">Se puede llamar a esta función varias veces para calcular el hash en flujos de datos largos o en flujos de datos descontinuos.</span><span class="sxs-lookup"><span data-stu-id="48a21-116">This function can be called multiple times to compute the hash on long data streams or discontinuous data streams.</span></span> <span data-ttu-id="48a21-117">Se debe llamar a la función [**\_ SHAFinal**](a-shafinal.md) antes de recuperar el valor hash.</span><span class="sxs-lookup"><span data-stu-id="48a21-117">The [**A\_SHAFinal**](a-shafinal.md) function must be called before retrieving the hash value.</span></span>

<span data-ttu-id="48a21-118">Esta función es muy similar a SHAUpdate, pero se llama directamente desde la biblioteca, en lugar de enrutarse a través de la infraestructura de criptografía.</span><span class="sxs-lookup"><span data-stu-id="48a21-118">This function is very similar to SHAUpdate, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="48a21-119">Para obtener más información, consulte [proveedores de Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="48a21-119">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="48a21-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48a21-120">Requirements</span></span>



| <span data-ttu-id="48a21-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a21-121">Requirement</span></span> | <span data-ttu-id="48a21-122">Value</span><span class="sxs-lookup"><span data-stu-id="48a21-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="48a21-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48a21-123">Header</span></span><br/>  | <dl> <span data-ttu-id="48a21-124"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="48a21-124"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="48a21-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48a21-125">Library</span></span><br/> | <dl> <span data-ttu-id="48a21-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48a21-126"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="48a21-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48a21-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="48a21-128"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48a21-128"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
