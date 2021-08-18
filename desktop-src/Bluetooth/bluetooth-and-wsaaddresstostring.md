---
title: Bluetooth y WSAAddressToString
description: La función WSAAddressToString Windows Sockets se usa para convertir una dirección de dispositivo de Bluetooth en una cadena, que a su vez se proporciona a la función WSALookupServiceBegin a través de la estructura WSAQUERYSET al recuperar información del servicio de dispositivo.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bb49563355b3a85ff64d7168f77e8526ca1679cffaa565e7b9cd7070cf87f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004285"
---
# <a name="bluetooth-and-wsaaddresstostring"></a>Bluetooth y WSAAddressToString

La función [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets se usa para convertir una dirección de dispositivo Bluetooth en una cadena, que a su vez se proporciona a la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) a través de la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) al recuperar información del servicio de dispositivo.

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

 

 