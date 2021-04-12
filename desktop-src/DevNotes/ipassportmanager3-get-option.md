---
description: Recupera el valor de una opción específica de inicio de sesión de Microsoft .NET Passport.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'IPassportManager3:: get_Option (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423199"
---
# <a name="ipassportmanager3get_option-method"></a><span data-ttu-id="f2e21-103">IPassportManager3:: get ( \_ método de opción)</span><span class="sxs-lookup"><span data-stu-id="f2e21-103">IPassportManager3::get\_Option method</span></span>

<span data-ttu-id="f2e21-104">Recupera el valor de una opción específica de inicio de sesión de Microsoft .NET Passport.</span><span class="sxs-lookup"><span data-stu-id="f2e21-104">Retrieves the value of a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="f2e21-105">El método **Get \_ Option** pertenece a la interfaz [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f2e21-105">The **get\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="f2e21-106">En este tema se complementa la documentación inicial.</span><span class="sxs-lookup"><span data-stu-id="f2e21-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f2e21-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2e21-107">Syntax</span></span>


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f2e21-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2e21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e21-109">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f2e21-109">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e21-110">Opción de inicio de sesión que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f2e21-110">The sign-in option to be retrieved.</span></span> <span data-ttu-id="f2e21-111">Actualmente, la única opción admitida es "iMode".</span><span class="sxs-lookup"><span data-stu-id="f2e21-111">Currently, the only supported option is "iMode".</span></span>

</dd> <dt>

<span data-ttu-id="f2e21-112">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f2e21-112">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e21-113">Un puntero a una **variante** (VT \_ bool) que recibe el valor de la opción.</span><span class="sxs-lookup"><span data-stu-id="f2e21-113">A pointer to a **VARIANT** (VT\_BOOL) that receives the value of the option.</span></span> <span data-ttu-id="f2e21-114">Este valor puede ser true o false.</span><span class="sxs-lookup"><span data-stu-id="f2e21-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e21-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2e21-115">Return value</span></span>

<span data-ttu-id="f2e21-116">Devuelve S \_ OK cuando el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="f2e21-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2e21-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2e21-117">Remarks</span></span>

<span data-ttu-id="f2e21-118">Este método se incluye con versiones anteriores del SDK de Passport.</span><span class="sxs-lookup"><span data-stu-id="f2e21-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
