---
title: Valores devueltos (características de accesibilidad de Windows)
description: En este tema se describen los valores devueltos más comunes y otros valores devueltos que puede ver con menos frecuencia.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0f073c401682eb78d9fdf9270709a84ed77ae2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443996"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="d26a5-103">Valores devueltos (características de accesibilidad de Windows)</span><span class="sxs-lookup"><span data-stu-id="d26a5-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="d26a5-104">En este tema se describen los valores devueltos más comunes y otros valores devueltos que puede ver con menos frecuencia.</span><span class="sxs-lookup"><span data-stu-id="d26a5-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="d26a5-105">Valores devueltos comunes</span><span class="sxs-lookup"><span data-stu-id="d26a5-105">Common Return Values</span></span>

<span data-ttu-id="d26a5-106">Los [**métodos IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) devuelven uno de los siguientes valores, definidos en winerror.h, u otro código de error estándar del Modelo de objetos componentes (COM):</span><span class="sxs-lookup"><span data-stu-id="d26a5-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|   <span data-ttu-id="d26a5-107">Valor</span><span class="sxs-lookup"><span data-stu-id="d26a5-107">Value</span></span>                      |   <span data-ttu-id="d26a5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d26a5-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d26a5-109">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="d26a5-109">S\_OK</span></span>                   | <span data-ttu-id="d26a5-110">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d26a5-110">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="d26a5-111">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="d26a5-111">S\_FALSE</span></span>                | <span data-ttu-id="d26a5-112">El método se ha instalado correctamente en parte.</span><span class="sxs-lookup"><span data-stu-id="d26a5-112">The method succeeded in part.</span></span> <span data-ttu-id="d26a5-113">Esto sucede cuando el método se realiza correctamente, pero la información solicitada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d26a5-113">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="d26a5-114">Por ejemplo, Microsoft Active Accessibility devuelve S FALSE si llama \_ a [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) para recuperar un objeto secundario en un punto determinado y el punto especificado no está dentro del objeto o del elemento secundario del objeto.</span><span class="sxs-lookup"><span data-stu-id="d26a5-114">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="d26a5-115">DISP \_ E \_ MEMBERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="d26a5-115">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="d26a5-116">El objeto no admite la propiedad o la acción solicitadas.</span><span class="sxs-lookup"><span data-stu-id="d26a5-116">The object does not support the requested property or action.</span></span> <span data-ttu-id="d26a5-117">Por ejemplo, un botón de inserción devuelve este valor si solicita su [propiedad Value](value-property.md), porque no tiene una propiedad Value.</span><span class="sxs-lookup"><span data-stu-id="d26a5-117">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="d26a5-118">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="d26a5-118">E\_NOTIMPL</span></span>              | <span data-ttu-id="d26a5-119">El método no está implementado.</span><span class="sxs-lookup"><span data-stu-id="d26a5-119">The method is not implemented.</span></span> <span data-ttu-id="d26a5-120">Este valor se produce cuando un cliente llama a un método que aún no se admite en ese sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d26a5-120">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d26a5-121">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d26a5-121">E\_INVALIDARG</span></span>           | <span data-ttu-id="d26a5-122">Uno o varios argumentos no eran válidos.</span><span class="sxs-lookup"><span data-stu-id="d26a5-122">One or more arguments were not valid.</span></span> <span data-ttu-id="d26a5-123">Este error se produce cuando el autor de la llamada intenta identificar un objeto secundario mediante un identificador que el servidor no reconoce.</span><span class="sxs-lookup"><span data-stu-id="d26a5-123">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="d26a5-124">Este error también se produce cuando un cliente intenta identificar un objeto secundario dentro de un objeto que no tiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="d26a5-124">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="d26a5-125">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d26a5-125">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="d26a5-126">El método no pudo asignar la memoria necesaria para completar una operación crucial para su éxito.</span><span class="sxs-lookup"><span data-stu-id="d26a5-126">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d26a5-127">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="d26a5-127">E\_FAIL</span></span>                 | <span data-ttu-id="d26a5-128">Se produjo un error desconocido o genérico.</span><span class="sxs-lookup"><span data-stu-id="d26a5-128">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="d26a5-129">Valores devueltos adicionales</span><span class="sxs-lookup"><span data-stu-id="d26a5-129">Additional Return Values</span></span>

<span data-ttu-id="d26a5-130">Los siguientes son valores devueltos que [**los métodos IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="d26a5-130">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="d26a5-131">Estos valores devueltos no son tan comunes como los anteriores, pero debe tener en cuenta estos valores.</span><span class="sxs-lookup"><span data-stu-id="d26a5-131">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|    <span data-ttu-id="d26a5-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d26a5-132">Value</span></span>                    |    <span data-ttu-id="d26a5-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="d26a5-133">Description</span></span>                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d26a5-134">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="d26a5-134">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="d26a5-135">Esto se devuelve cuando se llama a get \_ accValue para obtener el valor de un control de contraseña.</span><span class="sxs-lookup"><span data-stu-id="d26a5-135">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="d26a5-136">EXCEPCIÓN \_ DISP E \_</span><span class="sxs-lookup"><span data-stu-id="d26a5-136">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="d26a5-137">CO \_ E \_ OBJNOTCONNECTED</span><span class="sxs-lookup"><span data-stu-id="d26a5-137">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




