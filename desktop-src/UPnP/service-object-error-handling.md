---
title: Control de errores de objetos de servicio
description: Cuando se produce un error en un objeto de servicio, el valor devuelto para la llamada a IDispatch Invoke debe ser la \_ excepción DISP e \_ y se debe rellenar el puntero del parámetro pExceptInfo a una estructura EXCEPTINFO en.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd39d08dc7ca5152ca412df1a6fb67d6df524f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149353"
---
# <a name="service-object-error-handling"></a><span data-ttu-id="3c4be-103">Control de errores de objetos de servicio</span><span class="sxs-lookup"><span data-stu-id="3c4be-103">Service Object Error Handling</span></span>

<span data-ttu-id="3c4be-104">Cuando se produce un error en un objeto de servicio, el valor devuelto para la llamada a [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) debe ser la \_ excepción DISP e \_ y el puntero del parámetro *pExceptInfo* a una estructura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) en debe rellenarse.</span><span class="sxs-lookup"><span data-stu-id="3c4be-104">When an error occurs in a service object, the return value for the call [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) should be DISP\_E\_EXCEPTION, and the *pExceptInfo* parameter pointer to an [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) structure in the should be filled in.</span></span>

<span data-ttu-id="3c4be-105">Concretamente, el host del dispositivo usa los miembros **bstrSource** y **bstrDescription** de la estructura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) para crear una respuesta de error de UPnP. **bstrSource** es el código de error y **bstrDescription** es la descripción del error.</span><span class="sxs-lookup"><span data-stu-id="3c4be-105">Specifically, the **bstrSource**, and **bstrDescription** members of the [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) structure are used by the Device Host with UPnP technology to create a UPnP Fault response; **bstrSource** is the error code and **bstrDescription** is the error description.</span></span>

 

 