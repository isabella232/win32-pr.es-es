---
description: Obtiene una referencia a un objeto de controlador TCP V4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: ReferenceTcpDriver función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650161"
---
# <a name="referencetcpdriver-function"></a><span data-ttu-id="f942e-103">ReferenceTcpDriver función)</span><span class="sxs-lookup"><span data-stu-id="f942e-103">ReferenceTcpDriver function</span></span>

<span data-ttu-id="f942e-104">Obtiene una referencia a un objeto de controlador TCP V4.</span><span class="sxs-lookup"><span data-stu-id="f942e-104">Obtains a reference to a TCP v4 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f942e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f942e-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="f942e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f942e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f942e-107">*ppDriverObject* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f942e-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f942e-108">Puntero a una estructura **de \_ objeto de controlador** .</span><span class="sxs-lookup"><span data-stu-id="f942e-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="f942e-109">Para obtener más información, consulte la documentación del WDK.</span><span class="sxs-lookup"><span data-stu-id="f942e-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f942e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f942e-110">Return value</span></span>

<span data-ttu-id="f942e-111">Si la función se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f942e-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="f942e-112">Si se produce un error, devolverá el código de estado adecuado.</span><span class="sxs-lookup"><span data-stu-id="f942e-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f942e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f942e-113">Remarks</span></span>

<span data-ttu-id="f942e-114">Solo se puede llamar a esta función desde el modo kernel.</span><span class="sxs-lookup"><span data-stu-id="f942e-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="f942e-115">El autor de la llamada debe reducir el recuento de referencias mediante una llamada a la función **ObDereferenceObject** cuando ha terminado con el objeto.</span><span class="sxs-lookup"><span data-stu-id="f942e-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="f942e-116">Esta función se implementa en Drvref. lib, que está disponible para su descarga.</span><span class="sxs-lookup"><span data-stu-id="f942e-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="f942e-117">Vea [biblioteca de API de referencia de controladores de red de Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span><span class="sxs-lookup"><span data-stu-id="f942e-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="f942e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f942e-118">Requirements</span></span>



| <span data-ttu-id="f942e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f942e-119">Requirement</span></span> | <span data-ttu-id="f942e-120">Value</span><span class="sxs-lookup"><span data-stu-id="f942e-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f942e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f942e-121">Library</span></span><br/> | <dl> <span data-ttu-id="f942e-122"><dt>Drvref. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f942e-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f942e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f942e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f942e-124">**ReferenceTcpDriverV6**</span><span class="sxs-lookup"><span data-stu-id="f942e-124">**ReferenceTcpDriverV6**</span></span>](referencetcpdriverv6.md)
</dt> </dl>

 

 




