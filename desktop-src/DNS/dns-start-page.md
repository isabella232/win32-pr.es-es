---
title: Sistema de nombres de dominio
description: Sistema de nombres de dominio (DNS), un servicio de localizador de Microsoft Windows, es un protocolo estándar del sector que busca equipos en una red basada en IP.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS, (véase sistema de nombres de dominio)
- Sistema de nombres de dominio
- Sistema de nombres de dominio, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104083696"
---
# <a name="domain-name-system"></a>Sistema de nombres de dominio

## <a name="purpose"></a>Propósito

Sistema de nombres de dominio (DNS), un servicio de localizador de Microsoft Windows, es un protocolo estándar del sector que busca equipos en una red basada en IP. Las redes IP, como las redes de Internet y Windows, dependen de direcciones basadas en números para procesar los datos. Sin embargo, los usuarios pueden recordar más fácilmente las direcciones de nombre, por lo que es necesario traducir nombres descriptivos (como `www.microsoft.com` ) en direcciones que la red pueda reconocer (como 207.46.131.137).

## <a name="where-applicable"></a>Donde sea aplicable

Windows y Active Directory utilizan DNS. DNS es el servicio de localizador principal para Internet y Active Directory y, por tanto, DNS se considera un servicio base para Windows y Active Directory.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Windows proporciona funciones que permiten a los programadores de aplicaciones usar DNS, como consultas de DNS mediante programación, comparación de registros y búsqueda de nombres.

Los componentes DNS programables están diseñados para que puedan usarlos los programadores de C/C++. Para ello es necesario estar familiarizado con las redes y DNS. Los programadores deben estar familiarizados con el conjunto de protocolos IP, así como con el protocolo DNS y las operaciones DNS.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

DNS se usa en todas las redes IP que requieren un servicio de ubicación compatible con Internet. Sin embargo, la API de DNS requiere Windows 2000 o posterior.

## <a name="in-this-section"></a>En esta sección



| Tema                                                             | Descripción                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Documentos estándar de DNS](dns-standards-documents.md)<br/> | Vínculos a documentos estándar DNS públicos.<br/>                                  |
| [Acerca de DNS](about-dns.md)<br/>                             | Información general sobre DNS.<br/>                                            |
| [Referencia de DNS](dns-reference.md)<br/>                     | Documentación de referencia para DNS.<br/>                                          |
| [Proveedor WMI de DNS](dns-wmi-provider.md)<br/>               | Información general y documentación de referencia para el proveedor WMI de DNS.<br/> |
| [Glosario](glossary-gly.md)<br/>                           | Glosario de términos y definiciones de DNS.<br/>                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DHCP](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Aplicación auxiliar de protocolo de Internet](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

[Servicios de directorio](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)
</dt> </dl>

 

