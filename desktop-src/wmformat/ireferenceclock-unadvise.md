---
title: IReferenceClock unaconseje (método)
description: El método Unadvise cancela una solicitud de notificación.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Método unaconsej Windows Media Format
- Método unvise formato de Windows Media, interfaz IReferenceClock
- Interfaz IReferenceClock formato de Windows Media, método unvise
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148956"
---
# <a name="ireferenceclockunadvise-method"></a><span data-ttu-id="d8668-106">IReferenceClock:: Unadvise (método)</span><span class="sxs-lookup"><span data-stu-id="d8668-106">IReferenceClock::Unadvise method</span></span>

<span data-ttu-id="d8668-107">El método **Unadvise** cancela una solicitud de notificación.</span><span class="sxs-lookup"><span data-stu-id="d8668-107">The **Unadvise** method cancels a notification request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8668-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8668-108">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="d8668-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8668-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8668-110">*dwAdviseCookie*</span><span class="sxs-lookup"><span data-stu-id="d8668-110">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="d8668-111">Identificador de la solicitud que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="d8668-111">Identifier of the request to remove.</span></span> <span data-ttu-id="d8668-112">Use el valor devuelto por AdviseTime en el parámetro pdwAdviseCookie.</span><span class="sxs-lookup"><span data-stu-id="d8668-112">Use the value returned by AdviseTime in the pdwAdviseCookie parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8668-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8668-113">Return value</span></span>

<span data-ttu-id="d8668-114">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d8668-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d8668-115">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d8668-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d8668-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d8668-116">Return code</span></span>                                                                             | <span data-ttu-id="d8668-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8668-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="d8668-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d8668-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d8668-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d8668-119">The method succeeded.</span></span><br/>                    |
| <dl> <span data-ttu-id="d8668-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d8668-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d8668-121">El identificador pasado no existe.</span><span class="sxs-lookup"><span data-stu-id="d8668-121">The identifier passed in does not exist.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d8668-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8668-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8668-123">**Interfaz IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="d8668-123">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





