---
title: Acerca de DNS
description: El Sistema de nombres de dominio (DNS) es un protocolo estándar del sector que se usa para buscar equipos en una red basada en IP. Los usuarios pueden recordar nombres para mostrar, como www.microsoft.com que las direcciones basadas en números, como 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Acerca de DNS del sistema de nombres de dominio
- DNS del sistema de nombres de dominio , acerca de
- DNS del sistema de nombres de dominio , descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164754"
---
# <a name="about-dns"></a>Acerca de DNS

El Sistema de nombres de dominio (DNS) es un protocolo estándar del sector que se usa para buscar equipos en una red basada en IP. Los usuarios pueden recordar nombres para mostrar, por ejemplo, más fáciles que las direcciones basadas en números, como `www.microsoft.com` 207.46.131.137.

Las redes IP, como Internet y Windows, se basan en direcciones basadas en números para transmitir datos a través de la red. por lo tanto, es necesario traducir nombres para mostrar (como ) en direcciones numéricas que la red pueda reconocer `www.microsoft.com` (por ejemplo, 207.46.131.137). DNS es el servicio que se Windows para localizar estos recursos y traducirlos a direcciones IP.

DNS es el servicio de localizador principal para Active Directory y, por lo tanto, DNS se puede considerar un servicio base para Windows y Active Directory. Windows proporciona funciones que permiten a los programadores de aplicaciones usar funciones DNS, como realizar consultas DNS mediante programación, comparar registros y buscar nombres.

Muchas funciones DNS son realmente tipos de función, ya que hay un nombre base para la función, pero su uso depende de la codificación de caracteres. Por ejemplo, la función [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) aparece en la referencia de función de la interfaz de programación de aplicaciones (API) DNS como **DnsQuery**, pero su uso en las aplicaciones depende de si la codificación de caracteres es ANSI (designada anexando A al nombre del tipo de función), Unicode (designado anexando W al nombre del tipo de función) o \_ \_ UTF-8 (designado anexando UTF al nombre del tipo de \_ función). Por lo tanto, la llamada de función para **la función DnsQuery** sería realmente una de las siguientes:

DnsQuery \_ A ( A para la \_ codificación ANSI)

DnsQuery \_ W ( W para \_ codificación Unicode)

DnsQuery \_ UTF8 \_ (UTF8 para codificación UTF-8)

Todas las funciones que requieren esta convención muestran claramente este requisito dentro de las primeras oraciones de su definición de función. Use el nombre de función adecuado; Por ejemplo, no puede llamar simplemente [**a DnsQuery en**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) lugar de a DnsQuery \_ A.

 

 




