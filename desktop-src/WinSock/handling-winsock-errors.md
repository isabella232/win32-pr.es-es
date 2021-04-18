---
description: Control de errores en Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Control de errores de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705614"
---
# <a name="handling-winsock-errors"></a><span data-ttu-id="0e72e-103">Control de errores de Winsock</span><span class="sxs-lookup"><span data-stu-id="0e72e-103">Handling Winsock Errors</span></span>

<span data-ttu-id="0e72e-104">La mayoría de las funciones de Windows Sockets 2 no devuelven la causa específica de un error cuando la función devuelve.</span><span class="sxs-lookup"><span data-stu-id="0e72e-104">Most Windows Sockets 2 functions do not return the specific cause of an error when the function returns.</span></span> <span data-ttu-id="0e72e-105">Algunas funciones de Winsock devuelven un valor de cero si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="0e72e-105">Some Winsock functions return a value of zero if successful.</span></span> <span data-ttu-id="0e72e-106">De lo contrario, \_ se devuelve el valor de socket error (-1) y se puede recuperar un número de error concreto llamando a la función [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="0e72e-106">Otherwise, the value SOCKET\_ERROR (-1) is returned and a specific error number can be retrieved by calling the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function.</span></span> <span data-ttu-id="0e72e-107">En el caso de las funciones de Winsock que devuelven un identificador, un valor devuelto de Socket no válido \_ (0xFFFF) indica un error y se puede recuperar un número de error concreto llamando a **WSAGetLastError**.</span><span class="sxs-lookup"><span data-stu-id="0e72e-107">For Winsock functions that return a handle, a return value of INVALID\_SOCKET (0xffff) indicates an error and a specific error number can be retrieved by calling **WSAGetLastError**.</span></span> <span data-ttu-id="0e72e-108">En el caso de las funciones de Winsock que devuelven un puntero, un valor devuelto de **null** indica un error y se puede recuperar un número de error concreto llamando a la función **WSAGetLastError** .</span><span class="sxs-lookup"><span data-stu-id="0e72e-108">For Winsock functions that return a pointer, a return value of **NULL** indicates an error and a specific error number can be retrieved by calling the **WSAGetLastError** function.</span></span>

<span data-ttu-id="0e72e-109">Un código de error de Winsock se puede convertir en HRESULT para su uso en una llamada a procedimiento remoto (RPC) mediante HRESULT \_ de \_ Win32.</span><span class="sxs-lookup"><span data-stu-id="0e72e-109">A Winsock error code can be converted to an HRESULT for use in a remote procedure call (RPC) using HRESULT\_FROM\_WIN32.</span></span> <span data-ttu-id="0e72e-110">En versiones anteriores del kit de desarrollo de software (SDK) de la plataforma, HRESULT \_ de \_ Win32 se definía como una macro en el archivo de encabezado *Winerror. h* .</span><span class="sxs-lookup"><span data-stu-id="0e72e-110">In earlier versions of the Platform Software Development Kit (SDK), HRESULT\_FROM\_WIN32 was defined as a macro in the *Winerror.h* header file.</span></span> <span data-ttu-id="0e72e-111">En el kit de desarrollo de software (SDK) de Microsoft Windows, HRESULT \_ de \_ Win32 se define como una función insertada en el archivo de encabezado *Winerror. h* .</span><span class="sxs-lookup"><span data-stu-id="0e72e-111">In the Microsoft Windows Software Development Kit (SDK), HRESULT\_FROM\_WIN32 is defined as an inline function in the *Winerror.h* header file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e72e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e72e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e72e-113">Códigos de error de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="0e72e-113">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



