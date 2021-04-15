---
title: Valores devueltos (características de accesibilidad de Windows)
description: En este tema se describen los valores devueltos más comunes y otros valores devueltos que se pueden ver con menos frecuencia.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae2ccaf8bc74b1802be7569bc9e783cde4e11f9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488663"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="1e966-103">Valores devueltos (características de accesibilidad de Windows)</span><span class="sxs-lookup"><span data-stu-id="1e966-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="1e966-104">En este tema se describen los valores devueltos más comunes y otros valores devueltos que se pueden ver con menos frecuencia.</span><span class="sxs-lookup"><span data-stu-id="1e966-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="1e966-105">Valores devueltos comunes</span><span class="sxs-lookup"><span data-stu-id="1e966-105">Common Return Values</span></span>

<span data-ttu-id="1e966-106">Los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) devuelven uno de los valores siguientes, definidos en Winerror. h u otro código de error del modelo de objetos componentes (com) estándar:</span><span class="sxs-lookup"><span data-stu-id="1e966-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|                         |                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e966-107">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="1e966-107">S\_OK</span></span>                   | <span data-ttu-id="1e966-108">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="1e966-108">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="1e966-109">S \_ false</span><span class="sxs-lookup"><span data-stu-id="1e966-109">S\_FALSE</span></span>                | <span data-ttu-id="1e966-110">El método se realizó correctamente en parte.</span><span class="sxs-lookup"><span data-stu-id="1e966-110">The method succeeded in part.</span></span> <span data-ttu-id="1e966-111">Esto sucede cuando el método se ejecuta correctamente, pero la información solicitada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1e966-111">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="1e966-112">Por ejemplo, Microsoft Active Accessibility devuelve S \_ false si se llama a [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) para recuperar un objeto secundario en un punto determinado y el punto especificado no está dentro del objeto o del elemento secundario del objeto.</span><span class="sxs-lookup"><span data-stu-id="1e966-112">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="1e966-113">DISP \_ E \_ MEMBERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="1e966-113">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="1e966-114">El objeto no admite la propiedad o acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="1e966-114">The object does not support the requested property or action.</span></span> <span data-ttu-id="1e966-115">Por ejemplo, un botón de reenvío devuelve este valor si se solicita su [propiedad Value](value-property.md), ya que no tiene una propiedad Value.</span><span class="sxs-lookup"><span data-stu-id="1e966-115">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="1e966-116">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="1e966-116">E\_NOTIMPL</span></span>              | <span data-ttu-id="1e966-117">El método no está implementado.</span><span class="sxs-lookup"><span data-stu-id="1e966-117">The method is not implemented.</span></span> <span data-ttu-id="1e966-118">Este valor se produce cuando un cliente llama a un método que todavía no se admite en ese sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1e966-118">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="1e966-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1e966-119">E\_INVALIDARG</span></span>           | <span data-ttu-id="1e966-120">Uno o varios argumentos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="1e966-120">One or more arguments were not valid.</span></span> <span data-ttu-id="1e966-121">Este error se produce cuando el llamador intenta identificar un objeto secundario mediante un identificador que el servidor no reconoce.</span><span class="sxs-lookup"><span data-stu-id="1e966-121">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="1e966-122">Este error también se produce cuando un cliente intenta identificar un objeto secundario dentro de un objeto que no tiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="1e966-122">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="1e966-123">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="1e966-123">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="1e966-124">El método no pudo asignar la memoria necesaria para completar una operación fundamental para su éxito.</span><span class="sxs-lookup"><span data-stu-id="1e966-124">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1e966-125">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="1e966-125">E\_FAIL</span></span>                 | <span data-ttu-id="1e966-126">Se produjo un error desconocido o genérico.</span><span class="sxs-lookup"><span data-stu-id="1e966-126">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="1e966-127">Valores devueltos adicionales</span><span class="sxs-lookup"><span data-stu-id="1e966-127">Additional Return Values</span></span>

<span data-ttu-id="1e966-128">A continuación se muestran los valores devueltos que los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="1e966-128">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="1e966-129">Estos valores devueltos no son tan comunes como los anteriores, pero debe tenerlo en cuenta.</span><span class="sxs-lookup"><span data-stu-id="1e966-129">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|                        |                                                                                      |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1e966-130">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="1e966-130">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="1e966-131">Se devuelve cuando se llama a get \_ accValue para obtener el valor de un control de contraseña.</span><span class="sxs-lookup"><span data-stu-id="1e966-131">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="1e966-132">DISP \_ E ( \_ excepción)</span><span class="sxs-lookup"><span data-stu-id="1e966-132">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="1e966-133">CO \_ E \_ OBJNOTCONNECTED</span><span class="sxs-lookup"><span data-stu-id="1e966-133">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




