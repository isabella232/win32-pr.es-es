---
title: Bluetooth y WSAAddressToString
description: La función WSAAddressToString Windows Sockets se usa para convertir una dirección de dispositivo de Bluetooth en una cadena, que a su vez se proporciona a la función WSALookupServiceBegin a través de la estructura WSAQUERYSET al recuperar información del servicio del dispositivo.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e8a9ae3ea6a0f853619a3f3610a64204ad3c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172090"
---
# <a name="bluetooth-and-wsaaddresstostring"></a>Bluetooth y WSAAddressToString

La función [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets se usa para convertir una dirección de dispositivo de Bluetooth en una cadena, que a su vez se proporciona a la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) a través de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) al recuperar información del servicio del dispositivo.

Aunque una dirección de dispositivo Bluetooth se ajusta a un búfer de 20 caracteres, la función [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) devuelve actualmente **WSAEFAULT** para las direcciones de dispositivo de Bluetooth a menos que el búfer y el valor *lpdwAddressStringLength* especificado se establezcan en una longitud de caracteres de 40.

> [!Note]  
> Cuando **WSAEFAULT** devuelve [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) como resultado de un búfer insuficiente, el parámetro *lpdwAddressStringLength* no se actualiza con el tamaño de búfer necesario para la operación.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[Bluetooth y WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[Bluetooth y WSAQUERYSET](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 