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
# <a name="bluetooth-and-wsaaddresstostring"></a>Bluetooth y WSAAddressToString

La función [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) de Windows Sockets se usa para convertir una dirección de dispositivo Bluetooth en una cadena que, a su vez, se proporciona a la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) a través de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) al recuperar la información del servicio de dispositivo.

Mientras que una dirección de dispositivo Bluetooth cabe en un búfer de 20 caracteres, la función [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) devuelve actualmente **WSAEFAULT** para direcciones de dispositivo Bluetooth a menos que el búfer y el valor de *lpdwAddressStringLength* especificado se establezcan en una longitud de caracteres de 40.

> [!Note]  
> Cuando [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) devuelve **WSAEFAULT** como resultado de un búfer insuficiente, el parámetro *lpdwAddressStringLength* no se actualiza con el tamaño de búfer necesario para la operación.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[Bluetooth y WSAQUERYSET](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 