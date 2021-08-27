---
title: API de UPnP
description: El marco UPnP permite redes dinámicas de dispositivos inteligentes, dispositivos inalámbricos y equipos.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfadd64dbee845f62052e8b140ca1f0b69837ece78cf7b0cc5f24e61563a6e22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124805"
---
# <a name="upnp-apis"></a>API de UPnP

## <a name="purpose"></a>Propósito

El marco UPnP permite redes dinámicas de dispositivos inteligentes, dispositivos inalámbricos y equipos. Hay dos API para trabajar con dispositivos certificados por UPnP:

-   La API de punto de control, que consta de un conjunto de interfaces COM que se usan para buscar y controlar dispositivos.
-   La API de host de dispositivos, que consta de un conjunto de interfaces COM que se usan para implementar dispositivos hospedados por un equipo.

## <a name="where-applicable"></a>Donde sea aplicable

La API de punto de control permite a los desarrolladores escribir aplicaciones que buscan y controlan dispositivos certificados por UPnP. Device Host API permite a los desarrolladores implementar la funcionalidad de los dispositivos certificados por UPnP y usar el host del dispositivo para administrar las funciones de detección, descripción, control, presentación y eventos de un dispositivo con certificación UPnP.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Los desarrolladores que usan las API de punto de control y las API de host de dispositivo deben estar familiarizados con la arquitectura del dispositivo UPnP. Para obtener más información, vea la documentación de implementación de [UPnP](https://openconnectivity.org/resources/upnpresources.zip) y el foro [de UPnP](https://openconnectivity.org/).

Los desarrolladores que usan las API de host de dispositivo deben estar familiarizados con las interfaces Active Template Library (ATL) y COM.

Varias aplicaciones usan las API de punto de control y las API de host de dispositivos, desde scripts insertados en páginas HTML hasta programas completos de C++ y Microsoft Visual Basic.

Solo la API de punto de control admite Visual Basic Scripting Edition (VBScript).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API de punto de control se usa en equipos que ejecutan Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional y Windows CE .NET.

Device Host API se usa en equipos que ejecutan Windows XP, Windows XP Professional y Windows CE .NET.

Para obtener información más específica sobre qué sistemas operativos admiten una función determinada, consulte "Requisitos" en la documentación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                          | Descripción                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Introducción a la arquitectura de UPnP](overview-of-universal-plug-and-play.md)<br/>            | Información general y antecedentes.<br/>                                                     |
| [Información general sobre puntos de control](control-point-api.md)<br/>                                     | Información general sobre la API de punto de control.<br/>                                        |
| [Uso de la API de punto de control](using-the-control-point-api-with-upnp-technology.md)<br/> | Código de ejemplo que muestra cómo desarrollar aplicaciones que controlan dispositivos certificados por UPnP.<br/> |
| [Referencia de api de punto de control](control-point-api-with-upnp-technology-reference.md)<br/> | Documentación de interfaces, métodos y eventos de componentes de punto de control.<br/>               |
| [Introducción a la API de host de dispositivo](device-host-api.md)<br/>                                     | Información general sobre device host API.<br/>                                          |
| [Uso de device host API](using-the-device-host-api-with-upnp-technology.md)<br/>     | Código de ejemplo que muestra cómo desarrollar una aplicación para dispositivos con certificación UPnP.<br/>        |
| [Referencia de api de host de dispositivo](device-host-api-with-upnp-technology-reference.md)<br/>     | Documentación de interfaces, métodos y eventos de componentes de Host de dispositivo.<br/>                 |



 

 

 





