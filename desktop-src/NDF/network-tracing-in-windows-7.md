---
title: Seguimiento de red en Windows 7
description: Windows 7 se expande en el marco de diagnóstico de red (NDF) para proporcionar un método rápido para solucionar problemas de conectividad de red habilitando la recopilación de toda la información necesaria en un solo paso y aprovechando el seguimiento de eventos para Windows (ETW) para registrar paquetes de eventos de red en un solo archivo.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074209"
---
# <a name="network-tracing-in-windows-7"></a>Seguimiento de red en Windows 7

A medida que aumenta la complejidad de la pila de red, a menudo es difícil hacer un seguimiento rápido y diagnosticar problemas dentro de la pila. Windows 7 se expande en el marco de diagnóstico de red (NDF) para proporcionar un método rápido para solucionar problemas de conectividad de red habilitando la recopilación de toda la información necesaria en un solo paso y aprovechando el seguimiento de eventos para [Windows (ETW)](../etw/event-tracing-portal.md) para registrar eventos de red & paquetes en un solo archivo.

Los eventos y paquetes relacionados se agrupan para una actividad determinada, como la exploración de un sitio web, en los distintos componentes de la pila de redes. La salida de este proceso es un archivo de registro de seguimiento de eventos (ETL). Al permitir que todos los eventos relacionados con una actividad específica se puedan ver a la vez en este archivo, se puede reducir considerablemente el tiempo necesario para aislar y diagnosticar problemas de red.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [Seguimiento de red en Windows 7: Arquitectura](network-tracing-in-windows-7-architecture.md)                                |
| [Herramientas para solucionar problemas con el seguimiento de red en Windows 7](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [Seguimiento de red en Windows 7: escenarios](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 