---
title: API de UPnP
description: El entorno UPnP permite redes dinámicas de dispositivos inteligentes, dispositivos inalámbricos y PC.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104149705"
---
# <a name="upnp-apis"></a>API de UPnP

## <a name="purpose"></a>Propósito

El entorno UPnP permite redes dinámicas de dispositivos inteligentes, dispositivos inalámbricos y PC. Existen dos API para trabajar con dispositivos certificados con UPnP:

-   La API de punto de control, que consta de un conjunto de interfaces COM que se usan para buscar y controlar dispositivos.
-   La API del host del dispositivo, que consta de un conjunto de interfaces COM que se usan para implementar dispositivos hospedados por un equipo.

## <a name="where-applicable"></a>Donde sea aplicable

La API de punto de control permite a los desarrolladores escribir aplicaciones que busquen y controlen dispositivos certificados para UPnP. La API del host del dispositivo permite a los desarrolladores implementar la funcionalidad de los dispositivos certificados con UPnP y usar el host del dispositivo para administrar las funciones de detección, descripción, control, presentación y eventos de un dispositivo certificado con UPnP.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Los desarrolladores que usan las API del punto de control y las API de host del dispositivo deben estar familiarizados con la arquitectura del dispositivo UPnP. Para obtener más información, consulte la [documentación de implementación de UPnP](https://openconnectivity.org/resources/upnpresources.zip) y el foro de [UPnP](https://openconnectivity.org/).

Los desarrolladores que usan las API de host del dispositivo deben estar familiarizados con las interfaces de Active Template Library (ATL) y COM.

Las API de punto de control y las API de host de dispositivo se usan en una gran variedad de aplicaciones, desde scripts incrustados en páginas HTML hasta programas de C++ y Microsoft Visual Basic completos.

Solo la API del punto de control admite Visual Basic Scripting Edition (VBScript).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API de punto de control se usa en equipos que ejecutan Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional y Windows CE .NET.

La API del host del dispositivo se usa en equipos que ejecutan Windows XP, Windows XP Professional y Windows CE .NET.

Para obtener información más específica acerca de los sistemas operativos que admiten una función determinada, consulte "requisitos" en la documentación de.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                          | Descripción                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Información general sobre la arquitectura de UPnP](overview-of-universal-plug-and-play.md)<br/>            | Información general y fondo.<br/>                                                     |
| [Información general sobre puntos de control](control-point-api.md)<br/>                                     | Información general sobre la API de punto de control.<br/>                                        |
| [Uso de la API de punto de control](using-the-control-point-api-with-upnp-technology.md)<br/> | Código de ejemplo que muestra cómo desarrollar aplicaciones que controlan dispositivos certificados para UPnP.<br/> |
| [Referencia de API de punto de control](control-point-api-with-upnp-technology-reference.md)<br/> | Documentación de interfaces, métodos y eventos de componentes de punto de control.<br/>               |
| [Introducción a la API de host de dispositivo](device-host-api.md)<br/>                                     | Información general sobre la API del host del dispositivo.<br/>                                          |
| [Uso de la API del host del dispositivo](using-the-device-host-api-with-upnp-technology.md)<br/>     | Código de ejemplo que muestra cómo desarrollar una aplicación para dispositivos certificados para UPnP.<br/>        |
| [Referencia de API de host de dispositivo](device-host-api-with-upnp-technology-reference.md)<br/>     | Documentación de interfaces, métodos y eventos del componente host del dispositivo.<br/>                 |



 

 

 





