---
title: Arquitectura del administrador de lista de redes
description: Arquitectura del administrador de lista de redes
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567b103cfd5d9944aa33a799c2cc1bc4b983759
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994585"
---
# <a name="network-list-manager-architecture"></a>Arquitectura del administrador de lista de redes

Network List Manager se ejecuta como un servicio en el contexto de Svchost.exe y se inicia durante el procedimiento de arranque del equipo. El servicio Administrador de lista de redes mantiene una tabla de redes disponibles y los atributos de red que recuperan las aplicaciones a través de la API del administrador de lista de redes. Network List Manager proporciona funciones básicas para filtrar y consultar el servicio Administrador de lista de redes para redes específicas y recuperar los atributos de estas redes. En el diagrama siguiente se muestra la arquitectura del administrador de listas de redes y la interacción entre el servicio Administrador de lista de redes y la aplicación cliente.

![diagrama de arquitectura de reconocimiento de redes](images/architecture.png)

 

 




