---
title: El rol de administrador de lista de redes
description: El rol de administrador de lista de redes
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903872"
---
# <a name="the-role-of-network-list-manager"></a>El rol de administrador de lista de redes

Antes de Windows XP y Windows Server 2003, las aplicaciones tenían que llamar a varias API no relacionadas para obtener datos acerca de los atributos de red, como la dirección IP, el controlador de dominio o el sistema de nombres de dominio (DNS). A partir de Windows XP y Windows Server 2003, la API de reconocimiento de ubicación de red de Winsock incluye un conjunto limitado de funciones de ubicación de red. En Windows Server 2008 y Windows Vista, el servicio de reconocimiento de redes captura los atributos de red en una ubicación y permite que las aplicaciones consulten y recuperen redes y atributos específicos. El administrador de listas de redes reemplaza la funcionalidad de la API de Winsock anterior (disponible como proveedor de espacio de nombres de Winsock) al tiempo que mantiene la compatibilidad con aplicaciones anteriores mediante la API de Winsock.

 

 




