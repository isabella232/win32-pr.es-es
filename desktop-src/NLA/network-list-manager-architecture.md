---
title: Arquitectura del Administrador de listas de redes
description: Arquitectura del Administrador de listas de redes
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108ecbb36c5421bc7e3057c43feb10f92400493b306ecb21502a541c1bb4cba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685655"
---
# <a name="network-list-manager-architecture"></a>Arquitectura del Administrador de listas de redes

Network List Manager se ejecuta como un servicio en el contexto de Svchost.exe se inicia durante el procedimiento de arranque del equipo. El servicio Administrador de listas de redes mantiene una tabla de redes y atributos de red disponibles que las aplicaciones recuperan a través de network list manager API. Network List Manager proporciona funciones básicas para filtrar y consultar el servicio Network List Manager para redes específicas y recuperar los atributos de estas redes. En el diagrama siguiente se muestra la arquitectura del Administrador de listas de redes y la interacción entre el servicio Network List Manager y la aplicación cliente.

![diagrama de arquitectura de reconocimiento de red](images/architecture.png)

 

 




