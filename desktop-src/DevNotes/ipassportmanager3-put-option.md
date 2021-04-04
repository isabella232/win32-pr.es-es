---
description: Establece una opción específica de inicio de sesión de Microsoft .NET Passport.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3::p ut_Option método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998100"
---
# <a name="ipassportmanager3put_option-method"></a><span data-ttu-id="3151a-103">IPassportManager3::p \_ método de opción UT</span><span class="sxs-lookup"><span data-stu-id="3151a-103">IPassportManager3::put\_Option method</span></span>

<span data-ttu-id="3151a-104">Establece una opción específica de inicio de sesión de Microsoft .NET Passport.</span><span class="sxs-lookup"><span data-stu-id="3151a-104">Sets a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="3151a-105">El método **Put \_ Option** pertenece a la interfaz [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="3151a-105">The **put\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="3151a-106">En este tema se complementa la documentación inicial.</span><span class="sxs-lookup"><span data-stu-id="3151a-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3151a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3151a-107">Syntax</span></span>


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="3151a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3151a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3151a-109">*name*</span><span class="sxs-lookup"><span data-stu-id="3151a-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="3151a-110">Opción de inicio de sesión que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="3151a-110">The sign-in option to be set.</span></span> <span data-ttu-id="3151a-111">Actualmente, la única opción admitida es iMode.</span><span class="sxs-lookup"><span data-stu-id="3151a-111">Currently, the only supported option is iMode.</span></span>

</dd> <dt>

<span data-ttu-id="3151a-112">*newVal*</span><span class="sxs-lookup"><span data-stu-id="3151a-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="3151a-113">**Variant** (VT \_ bool) que especifica el nuevo valor de la opción.</span><span class="sxs-lookup"><span data-stu-id="3151a-113">A **VARIANT** (VT\_BOOL) that specifies the new value for the option.</span></span> <span data-ttu-id="3151a-114">Este valor puede ser true o false.</span><span class="sxs-lookup"><span data-stu-id="3151a-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3151a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3151a-115">Return value</span></span>

<span data-ttu-id="3151a-116">Devuelve S \_ OK cuando el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="3151a-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="3151a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3151a-117">Remarks</span></span>

<span data-ttu-id="3151a-118">Este método se incluye con versiones anteriores del SDK de Passport.</span><span class="sxs-lookup"><span data-stu-id="3151a-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
