---
title: Qué ve un cliente
description: En este tema se enumeran las formas en que un cliente ve datos ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, qué ve un cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533495"
---
# <a name="what-does-a-client-see"></a><span data-ttu-id="65eae-104">¿Qué ve un cliente?</span><span class="sxs-lookup"><span data-stu-id="65eae-104">What Does a Client See?</span></span>

-   <span data-ttu-id="65eae-105">Un cliente ve ADSI y todos sus objetos de extensión como un objeto.</span><span class="sxs-lookup"><span data-stu-id="65eae-105">A client sees ADSI and all of its extension objects as one object.</span></span>
-   <span data-ttu-id="65eae-106">Un cliente ADSI ve una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que controla todas las interfaces de distribución y dual en el objeto, independientemente de si el agregador implementa la interfaz dual o de distribución en el proveedor o mediante una extensión.</span><span class="sxs-lookup"><span data-stu-id="65eae-106">An ADSI client sees one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface that handles all the dual and dispatch interfaces in the object, whether the dual or dispatch interface is implemented by the aggregator in the provider or by an extension.</span></span> <span data-ttu-id="65eae-107">Consulte [resolución de conflictos de nombres de función y propiedad en la automatización en las extensiones](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="65eae-107">Please see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>
-   <span data-ttu-id="65eae-108">ADSI no expone ninguna información de tipo a través de los métodos [**IDispatch:: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) o [**IDispatch:: GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) .</span><span class="sxs-lookup"><span data-stu-id="65eae-108">ADSI does not expose any type information through the [**IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) or [**IDispatch::GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) methods.</span></span> <span data-ttu-id="65eae-109">ADSI proporciona información de tipos a través de la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="65eae-109">ADSI provides type information through the type library.</span></span>

 

 