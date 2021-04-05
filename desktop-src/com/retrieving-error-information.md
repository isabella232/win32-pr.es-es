---
title: Recuperar información sobre errores
description: Recuperar información sobre errores
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078399"
---
# <a name="retrieving-error-information"></a><span data-ttu-id="89533-103">Recuperar información sobre errores</span><span class="sxs-lookup"><span data-stu-id="89533-103">Retrieving Error Information</span></span>

<span data-ttu-id="89533-104">Mediante las interfaces y funciones de control de errores COM, puede recuperar la información de error de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="89533-104">Using the COM error-handling interfaces and functions, you can retrieve error information as follows:</span></span>

1.  <span data-ttu-id="89533-105">Compruebe si el valor devuelto representa un error que el objeto está preparado para controlar.</span><span class="sxs-lookup"><span data-stu-id="89533-105">Check whether the returned value represents an error that the object is prepared to handle.</span></span>
2.  <span data-ttu-id="89533-106">Llame a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero a la interfaz [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="89533-106">Call [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span> <span data-ttu-id="89533-107">A continuación, llame a [**ISupportErrorInfo:: InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) para comprobar que el error lo ha producido el objeto que lo devolvió y que el objeto de error pertenece al error actual y no a una llamada anterior.</span><span class="sxs-lookup"><span data-stu-id="89533-107">Then call [**ISupportErrorInfo::InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) to verify that the error was raised by the object that returned it and that the error object pertains to the current error and not to a previous call.</span></span>
3.  <span data-ttu-id="89533-108">Para obtener un puntero al objeto de error, llame a la función [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="89533-108">To get a pointer to the error object, call the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function.</span></span>
4.  <span data-ttu-id="89533-109">Para recuperar información del objeto de error, use los métodos [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="89533-109">To retrieve information from the error object, use the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) methods.</span></span>

<span data-ttu-id="89533-110">Si el objeto no está preparado para controlar el error, pero necesita propagar la información de error más abajo en la cadena de llamadas, simplemente debe pasar el valor devuelto a su llamador.</span><span class="sxs-lookup"><span data-stu-id="89533-110">If the object is not prepared to handle the error but needs to propagate the error information further down the call chain, it should simply pass the return value to its caller.</span></span> <span data-ttu-id="89533-111">Dado que la función [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) borra la información de error y pasa la propiedad del objeto de error al autor de la llamada, solo el objeto que controla el error debe llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="89533-111">Because the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function clears the error information and passes ownership of the error object to the caller, the function should be called only by the object that handles the error.</span></span>

 

 