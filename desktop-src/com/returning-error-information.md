---
title: Devolver información de error
description: Devolver información de error
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421439"
---
# <a name="returning-error-information"></a><span data-ttu-id="394c9-103">Devolver información de error</span><span class="sxs-lookup"><span data-stu-id="394c9-103">Returning Error Information</span></span>

<span data-ttu-id="394c9-104">Mediante las interfaces y funciones de control de errores de COM, puede devolver información de error realizando los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="394c9-104">Using the COM error-handling interfaces and functions, you can return error information by performing the following the steps:</span></span>

1.  <span data-ttu-id="394c9-105">Implemente la interfaz [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="394c9-105">Implement the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span>
2.  <span data-ttu-id="394c9-106">Para crear una instancia del objeto de error genérico, llame a la función [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="394c9-106">To create an instance of the generic error object, call the [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) function.</span></span>
3.  <span data-ttu-id="394c9-107">Para establecer su contenido, use los métodos [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="394c9-107">To set its contents, use the [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) methods.</span></span>
4.  <span data-ttu-id="394c9-108">Para asociar el objeto de error al subproceso lógico actual, llame a la función [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="394c9-108">To associate the error object with the current logical thread, call the [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) function.</span></span>

<span data-ttu-id="394c9-109">Las interfaces de control de errores crean y administran un objeto de error, que proporciona información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="394c9-109">The error handling interfaces create and manage an error object, which provides information about the error.</span></span> <span data-ttu-id="394c9-110">El objeto de error no es el mismo que el objeto que encontró el error.</span><span class="sxs-lookup"><span data-stu-id="394c9-110">The error object is not the same as the object that encountered the error.</span></span> <span data-ttu-id="394c9-111">Es un objeto independiente asociado al subproceso de ejecución actual.</span><span class="sxs-lookup"><span data-stu-id="394c9-111">It is a separate object associated with the current thread of execution.</span></span>

 

 