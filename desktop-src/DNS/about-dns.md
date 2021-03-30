---
title: Acerca de DNS
description: El sistema de nombres de dominio (DNS) es un protocolo estándar del sector que se usa para buscar equipos en una red basada en IP. Los usuarios pueden recordar nombres para mostrar, como www.microsoft.com más fácilmente que las direcciones basadas en números, como 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Acerca del DNS del sistema de nombres de dominio
- Sistema de nombres de dominio DNS, acerca de
- DNS del sistema de nombres de dominio, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104280212"
---
# <a name="about-dns"></a>Acerca de DNS

El sistema de nombres de dominio (DNS) es un protocolo estándar del sector que se usa para buscar equipos en una red basada en IP. Los usuarios pueden recordar los nombres para mostrar, como `www.microsoft.com` más sencillo que las direcciones basadas en números, como 207.46.131.137.

Las redes IP, como las redes de Internet y Windows, dependen de direcciones basadas en números para transmitir datos a través de la red. por lo tanto, es necesario traducir los nombres para mostrar (como `www.microsoft.com` ) en direcciones numéricas que la red pueda reconocer (como 207.46.131.137). DNS es el servicio preferido en Windows para localizar estos recursos y traducirlos en direcciones IP.

DNS es el servicio de localizador principal para Active Directory y, por tanto, el DNS se puede considerar como un servicio base para Windows y para Active Directory. Windows proporciona funciones que permiten a los programadores de aplicaciones usar funciones de DNS, como la realización de consultas de DNS mediante programación, la comparación de registros y la búsqueda de nombres.

Muchas funciones de DNS son realmente tipos de función, en que hay un nombre base para la función, pero su uso depende de la codificación de caracteres. Por ejemplo, la función [**dnsquery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) aparece en la referencia de funciones de la interfaz de programación de aplicaciones (API) DNS como **DnsQuery**. pero su uso en las aplicaciones depende de si la codificación de caracteres es ANSI (designada mediante la anexión de \_ un al nombre de tipo de función), Unicode (designado mediante anexando \_ W al nombre de tipo de función) o UTF-8 (designado mediante la anexión de \_ UTF al nombre de tipo de función). Por lo tanto, la llamada de función para la función **DnsQuery** sería realmente una de las siguientes:

DnsQuery \_ a ( \_ para la codificación ANSI)

DnsQuery \_ w ( \_ w para codificación Unicode)

DnsQuery \_ UTF8 ( \_ UTF8 para la codificación UTF-8)

Todas las funciones que requieren esta Convención indican claramente este requisito en las primeras oraciones de la definición de función. Use el nombre de función adecuado; por ejemplo, no puede llamar simplemente a [**dnsquery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) en lugar de a dnsquery \_ a.

 

 




