---
title: El rol del Administrador de listas de redes
description: El rol del Administrador de listas de redes
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec37d0cf157b87bf43fe12e9aa3a33eb316b7800474dd75ef3a6d4e23bb6189d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780495"
---
# <a name="the-role-of-network-list-manager"></a>El rol del Administrador de listas de redes

Antes de Windows XP y Windows Server 2003, las aplicaciones tenían que llamar a varias API no relacionadas para obtener datos sobre atributos de red como la dirección IP, el controlador de dominio o el sistema de nombres de dominio (DNS). A partir de Windows XP y Windows Server 2003, la API Winsock de reconocimiento de ubicación de red presentaba un conjunto limitado de funcionalidades de ubicación de red. En Windows Server 2008 y Windows Vista, el servicio Network Awareness captura los atributos de red en una ubicación y permite a las aplicaciones consultar y recuperar atributos y redes específicos. Network List Manager reemplaza la funcionalidad de la API winsock anterior (disponible como proveedor de espacio de nombres de Winsock) al tiempo que mantiene la compatibilidad con aplicaciones anteriores mediante winsock API.

 

 




