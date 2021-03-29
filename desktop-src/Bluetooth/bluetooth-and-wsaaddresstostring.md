---
title: Bluetooth y WSAAddressToString
description: La función WSAAddressToString de Windows Sockets se usa para convertir una dirección de dispositivo Bluetooth en una cadena que, a su vez, se proporciona a la función WSALookupServiceBegin a través de la estructura WSAQUERYSET al recuperar la información del servicio de dispositivo.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e8a9ae3ea6a0f853619a3f3610a64204ad3c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077832"
---
# <a name="bluetooth-and-wsaaddresstostring"></a><span data-ttu-id="cc3fd-103">Bluetooth y WSAAddressToString</span><span class="sxs-lookup"><span data-stu-id="cc3fd-103">Bluetooth and WSAAddressToString</span></span>

<span data-ttu-id="cc3fd-104">La función [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) de Windows Sockets se usa para convertir una dirección de dispositivo Bluetooth en una cadena que, a su vez, se proporciona a la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) a través de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) al recuperar la información del servicio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc3fd-104">The [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets function is used to convert a Bluetooth Device Address to a string, which is in turn provided to the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function via the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure when retrieving device service information.</span></span>

<span data-ttu-id="cc3fd-105">Mientras que una dirección de dispositivo Bluetooth cabe en un búfer de 20 caracteres, la función [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) devuelve actualmente **WSAEFAULT** para direcciones de dispositivo Bluetooth a menos que el búfer y el valor de *lpdwAddressStringLength* especificado se establezcan en una longitud de caracteres de 40.</span><span class="sxs-lookup"><span data-stu-id="cc3fd-105">While a Bluetooth Device Address fits within a 20 character buffer, the [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) function currently returns **WSAEFAULT** for Bluetooth Device Addresses unless the buffer and the specified *lpdwAddressStringLength* value are set to a character length of 40.</span></span>

> [!Note]  
> <span data-ttu-id="cc3fd-106">Cuando [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) devuelve **WSAEFAULT** como resultado de un búfer insuficiente, el parámetro *lpdwAddressStringLength* no se actualiza con el tamaño de búfer necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="cc3fd-106">When **WSAEFAULT** is returned by [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) as the result of an insufficient buffer, the *lpdwAddressStringLength* parameter is not updated with the buffer size required for the operation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cc3fd-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc3fd-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc3fd-108">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="cc3fd-108">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="cc3fd-109">Bluetooth y WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="cc3fd-109">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="cc3fd-110">Bluetooth y WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="cc3fd-110">Bluetooth and WSAQUERYSET</span></span>](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 