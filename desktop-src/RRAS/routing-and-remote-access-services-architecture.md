---
title: Arquitectura de enrutamiento y Access Services remota
description: En la ilustración siguiente se presenta una vista general de la arquitectura del Windows 2000.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, RRAS de enrutamiento y Access Services arquitectura remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062768"
---
# <a name="routing-and-remote-access-services-architecture"></a>Arquitectura de enrutamiento y Access Services remota

En la ilustración siguiente se presenta una vista general de la arquitectura del Windows 2000.

Los componentes específicos de la familia de protocolos IP se muestran en gris claro. Los componentes específicos de la familia de protocolos IPX se muestran en gris oscuro. Los componentes que son generales para todas las familias de protocolos no se tienen en cuenta.

El servicio de enrutamiento y acceso remoto proporciona API para administrar y configurar el servicio. Estas API incluyen agentes SNMP para IP e IPX.

RRAS incluye protocolos de enrutamiento para IP e IPX. Para IP, RRAS proporciona los protocolos de enrutamiento Protocolo de información de enrutamiento (RIP) y Open Shortest Path First (OSPF). Para IPX, RRAS proporciona IPX RIP y Service Advertising Protocol (SAP).

RRAS usa un Administrador de tablas de enrutamiento (RTM) para IP e IPX. Sin embargo, cada familia de protocolos tiene su propio administrador de enrutadores. RRAS también tiene un componente independiente para administrar grupos de multidifusión.

Las interfaces del Administrador de interfaces dinámicas (DIM) con servicios PPP y TAPI para administrar las interfaces PPP que usan algunas rutas.

![vista de arquitectura general del enrutador de Windows 2000](images/rtarch.png)

 

 




