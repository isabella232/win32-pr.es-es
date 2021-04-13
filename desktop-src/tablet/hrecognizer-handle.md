---
description: Un identificador HRECOGNIZER se usa para crear un contexto de reconocedor, recuperar los atributos y propiedades del reconocedor, y determinar qué propiedades de paquete requiere el reconocedor para realizar el reconocimiento.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Identificador de HRECOGNIZER (Resumen. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360348"
---
# <a name="hrecognizer-handle"></a><span data-ttu-id="9584e-103">Identificador de HRECOGNIZER</span><span class="sxs-lookup"><span data-stu-id="9584e-103">HRECOGNIZER Handle</span></span>

<span data-ttu-id="9584e-104">Un identificador **HRECOGNIZER** se usa para crear un contexto de reconocedor, recuperar los atributos y propiedades del reconocedor, y determinar qué propiedades de paquete requiere el reconocedor para realizar el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="9584e-104">An **HRECOGNIZER** handle is used to create a recognizer context, retrieve the recognizer's attributes and properties, and determine which packet properties the recognizer requires to perform recognition.</span></span>


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a><span data-ttu-id="9584e-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9584e-105">Remarks</span></span>

<span data-ttu-id="9584e-106">Las siguientes funciones usan un **HRECOGNIZER**.</span><span class="sxs-lookup"><span data-stu-id="9584e-106">The following functions use an **HRECOGNIZER**.</span></span>



| <span data-ttu-id="9584e-107">Función</span><span class="sxs-lookup"><span data-stu-id="9584e-107">Function</span></span>                                                               | <span data-ttu-id="9584e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9584e-108">Description</span></span>                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9584e-109">**CreateRecognizer**</span><span class="sxs-lookup"><span data-stu-id="9584e-109">**CreateRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | <span data-ttu-id="9584e-110">Crea un reconocedor.</span><span class="sxs-lookup"><span data-stu-id="9584e-110">Creates a recognizer.</span></span><br/>                                                                   |
| [<span data-ttu-id="9584e-111">**DestroyRecognizer**</span><span class="sxs-lookup"><span data-stu-id="9584e-111">**DestroyRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | <span data-ttu-id="9584e-112">Destruye un reconocedor.</span><span class="sxs-lookup"><span data-stu-id="9584e-112">Destroys a recognizer.</span></span><br/>                                                                  |
| [<span data-ttu-id="9584e-113">**GetRecoAttributes**</span><span class="sxs-lookup"><span data-stu-id="9584e-113">**GetRecoAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | <span data-ttu-id="9584e-114">Devuelve los atributos del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="9584e-114">Returns the attributes of the recognizer.</span></span><br/>                                               |
| [<span data-ttu-id="9584e-115">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="9584e-115">**CreateContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | <span data-ttu-id="9584e-116">Crea un contexto de reconocedor.</span><span class="sxs-lookup"><span data-stu-id="9584e-116">Creates a recognizer context.</span></span><br/>                                                           |
| [<span data-ttu-id="9584e-117">**DestroyContext**</span><span class="sxs-lookup"><span data-stu-id="9584e-117">**DestroyContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | <span data-ttu-id="9584e-118">Destruye un contexto de reconocedor.</span><span class="sxs-lookup"><span data-stu-id="9584e-118">Destroys a recognizer context.</span></span><br/>                                                          |
| [<span data-ttu-id="9584e-119">**GetAllRecognizers**</span><span class="sxs-lookup"><span data-stu-id="9584e-119">**GetAllRecognizers**</span></span>](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | <span data-ttu-id="9584e-120">Obtiene todos los reconocedores.</span><span class="sxs-lookup"><span data-stu-id="9584e-120">Gets all recognizers.</span></span><br/>                                                                   |
| [<span data-ttu-id="9584e-121">**GetResultPropertyList**</span><span class="sxs-lookup"><span data-stu-id="9584e-121">**GetResultPropertyList**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | <span data-ttu-id="9584e-122">Recupera una lista de propiedades que el reconocedor puede devolver para un intervalo de resultados.</span><span class="sxs-lookup"><span data-stu-id="9584e-122">Retrieves a list of properties the recognizer can return for a result range.</span></span><br/>            |
| [<span data-ttu-id="9584e-123">**GetPreferredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="9584e-123">**GetPreferredPacketDescription**</span></span>](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | <span data-ttu-id="9584e-124">Recupera una descripción de paquete que contiene las propiedades de paquete que utiliza el reconocedor.</span><span class="sxs-lookup"><span data-stu-id="9584e-124">Retrieves a packet description that contains the packet properties the recognizer uses.</span></span><br/> |
| [<span data-ttu-id="9584e-125">**GetUnicodeRanges**</span><span class="sxs-lookup"><span data-stu-id="9584e-125">**GetUnicodeRanges**</span></span>](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | <span data-ttu-id="9584e-126">Recupera los intervalos de puntos Unicode que admite el reconocedor.</span><span class="sxs-lookup"><span data-stu-id="9584e-126">Retrieves the ranges of Unicode points that the recognizer supports.</span></span><br/>                    |
| [<span data-ttu-id="9584e-127">**LoadCachedAttributes**</span><span class="sxs-lookup"><span data-stu-id="9584e-127">**LoadCachedAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | <span data-ttu-id="9584e-128">Carga los atributos almacenados en memoria caché de un reconocedor.</span><span class="sxs-lookup"><span data-stu-id="9584e-128">Loads the cached attributes of a recognizer.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="9584e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9584e-129">Requirements</span></span>



| <span data-ttu-id="9584e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9584e-130">Requirement</span></span> | <span data-ttu-id="9584e-131">Value</span><span class="sxs-lookup"><span data-stu-id="9584e-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9584e-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9584e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9584e-133">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9584e-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="9584e-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9584e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9584e-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9584e-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="9584e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9584e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9584e-137"><dt>Resumen. h</dt></span><span class="sxs-lookup"><span data-stu-id="9584e-137"><dt>Recapis.h</dt></span></span> </dl> |



 

 




