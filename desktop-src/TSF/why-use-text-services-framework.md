---
title: Por qué usar el marco de trabajo de servicios de texto
description: Por qué usar el marco de trabajo de servicios de texto
ms.assetid: 64b3b0a1-7740-49fa-b0a6-f80040147280
keywords:
- Marco de trabajo de servicios de texto (TSF), acerca de
- TSF (marco de trabajo de servicios de texto), acerca de
- servicios de texto, acerca de
- Aplicaciones habilitadas para TSF, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6647981b890bd1fcdf488b18bffad587f49ed9b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685482"
---
# <a name="why-use-text-services-framework"></a>¿Por qué usar el marco de trabajo de servicios de texto?

El marco de trabajo de servicios de texto (TSF) permite que una aplicación habilitada para TSF reciba entradas de texto de cualquier número de dispositivos o orígenes. Dado que TSF es extensible, la aplicación puede recibir entradas de texto de orígenes de texto adicionales con poca o ninguna modificación.

Un servicio de texto obtiene texto de y proporciona texto a cualquier aplicación habilitada para TSF sin necesidad de ningún conocimiento sobre la aplicación. Esta estructura permite que el servicio de texto esté disponible para cualquier aplicación habilitada para TSF. El servicio de texto se puede instalar o actualizar como un módulo independiente y es independiente de cualquier aplicación específica. TSF también permite a un servicio de texto almacenar metadatos con un documento, un fragmento de texto o un objeto dentro del documento. Por ejemplo, un servicio de texto de entrada de voz puede almacenar información de sonido asociada a un bloque de texto.

TSF permite a los servicios de texto proporcionar una conversión de texto precisa y completa, con acceso continuo al búfer del documento. Los servicios de texto que usan TSF pueden evitar separar su funcionalidad en modos de entrada y de modo de edición. Esta arquitectura de entrada permite que el flujo de texto almacenado en búfer y acumulado Cambie dinámicamente, lo que permite una edición de texto y una entrada de teclado más eficientes.

TSF es independiente del dispositivo y habilita los servicios de texto para varios dispositivos de entrada, como el teclado, el lápiz y el micrófono.

 

 




