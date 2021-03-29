---
description: Obtiene una referencia a un objeto de controlador de TCP V6.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: ReferenceTcpDriverV6 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650131"
---
# <a name="referencetcpdriverv6-function"></a><span data-ttu-id="80618-103">ReferenceTcpDriverV6 función)</span><span class="sxs-lookup"><span data-stu-id="80618-103">ReferenceTcpDriverV6 function</span></span>

<span data-ttu-id="80618-104">Obtiene una referencia a un objeto de controlador de TCP V6.</span><span class="sxs-lookup"><span data-stu-id="80618-104">Obtains a reference to a TCP v6 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="80618-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80618-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="80618-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80618-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80618-107">*ppDriverObject* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="80618-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80618-108">Puntero a una estructura **de \_ objeto de controlador** .</span><span class="sxs-lookup"><span data-stu-id="80618-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="80618-109">Para obtener más información, consulte la documentación del WDK.</span><span class="sxs-lookup"><span data-stu-id="80618-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80618-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80618-110">Return value</span></span>

<span data-ttu-id="80618-111">Si la función se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="80618-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="80618-112">Si se produce un error, devolverá el código de estado adecuado.</span><span class="sxs-lookup"><span data-stu-id="80618-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="80618-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80618-113">Remarks</span></span>

<span data-ttu-id="80618-114">Solo se puede llamar a esta función desde el modo kernel.</span><span class="sxs-lookup"><span data-stu-id="80618-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="80618-115">El autor de la llamada debe reducir el recuento de referencias mediante una llamada a la función **ObDereferenceObject** cuando ha terminado con el objeto.</span><span class="sxs-lookup"><span data-stu-id="80618-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="80618-116">Esta función se implementa en Drvref. lib, que está disponible para su descarga.</span><span class="sxs-lookup"><span data-stu-id="80618-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="80618-117">Vea [biblioteca de API de referencia de controladores de red de Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span><span class="sxs-lookup"><span data-stu-id="80618-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="80618-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80618-118">Requirements</span></span>



| <span data-ttu-id="80618-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="80618-119">Requirement</span></span> | <span data-ttu-id="80618-120">Value</span><span class="sxs-lookup"><span data-stu-id="80618-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80618-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80618-121">Library</span></span><br/> | <dl> <span data-ttu-id="80618-122"><dt>Drvref. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80618-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80618-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="80618-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80618-124">**ReferenceTcpDriver**</span><span class="sxs-lookup"><span data-stu-id="80618-124">**ReferenceTcpDriver**</span></span>](referencetcpdriver.md)
</dt> </dl>

 

 




