---
title: Arquitectura de mezclador
description: Arquitectura de mezclador
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- audio multimedia, arquitectura de mezclador
- arquitectura de audio y mezclador
- Mezcladores de audio, arquitectura
- Mezcladores de audio, líneas de audio
- líneas de audio
- Mezcladores de audio, controles
- audio multimedia, controles de mezclador
- audio, controles de mezclador
- mezcladores, líneas de audio
- mezcladores, arquitectura
- mezcladores, controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357049"
---
# <a name="mixer-architecture"></a>Arquitectura de mezclador

El elemento básico de la arquitectura del mezclador es una *línea de audio*. Una línea de audio se compone de uno o varios canales de datos procedentes de un único origen o de un recurso del sistema. Por ejemplo, una línea de audio estéreo tiene dos canales de datos, pero se considera una sola línea de audio porque se origina a partir de un único origen.

La arquitectura del mezclador proporciona servicios de enrutamiento para administrar las líneas de audio de un equipo. Puede usar los servicios de enrutamiento si tiene instalados los dispositivos de hardware y los controladores de software adecuados. La arquitectura del mezclador permite que varias líneas de origen de audio se asignen a una sola línea de audio de destino.

Cada línea de audio puede tener controles de mezclador asociados. Un control de mezclador puede realizar cualquier número de funciones (como el volumen del control), en función de las características de la línea de audio asociada.

 

 




