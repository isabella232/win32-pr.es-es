---
title: Arquitectura de servicios de enrutamiento y acceso remoto
description: En la ilustración siguiente se muestra una vista arquitectónica general del enrutador 2000 de Windows.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- RRAS del servicio de enrutamiento y acceso remoto RRAS, arquitectura de servicios de enrutamiento y acceso remoto RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486919"
---
# <a name="routing-and-remote-access-services-architecture"></a>Arquitectura de servicios de enrutamiento y acceso remoto

En la ilustración siguiente se muestra una vista arquitectónica general del enrutador 2000 de Windows.

Los componentes que son específicos de la familia del protocolo IP se muestran en gris claro. Los componentes que son específicos de la familia de protocolos IPX se muestran en gris oscuro. Los componentes que son generales para todas las familias de protocolos no están sombreados.

El servicio de enrutamiento y acceso remoto proporciona las API para administrar y configurar el servicio. Estas API incluyen agentes SNMP para IP e IPX.

RRAS incluye protocolos de enrutamiento para IP e IPX. Para IP, RRAS proporciona los protocolos de enrutamiento protocolo de información de enrutamiento (RIP) y ruta de acceso más corta (OSPF). Para IPX, RRAS proporciona IPX RIP y el protocolo de anuncio de servicio (SAP).

RRAS usa un administrador de tabla de enrutamiento (RTM) para IP e IPX. Sin embargo, cada familia de protocolos tiene su propio administrador de enrutadores. RRAS también tiene un componente independiente para administrar grupos de multidifusión.

Las interfaces de Dynamic interface Manager (DIM) con servicios PPP y TAPI para administrar las interfaces PPP utilizadas por algunas rutas.

![vista arquitectónica general del enrutador de Windows 2000](images/rtarch.png)

 

 




