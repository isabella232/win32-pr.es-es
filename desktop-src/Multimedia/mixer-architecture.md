---
title: Mixer Arquitectura
description: Mixer Arquitectura
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- audio multimedia, arquitectura mezcladora
- audio, arquitectura mezcladora
- mezcladores de audio, arquitectura
- mezcladores de audio, líneas de audio
- líneas de audio
- mezcladores de audio, controles
- audio multimedia, controles mezcladores
- audio, controles mezcladores
- mezcladores, líneas de audio
- mezcladores, arquitectura
- mezcladores, controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372379"
---
# <a name="mixer-architecture"></a>Mixer Arquitectura

El elemento básico de la arquitectura del mezclador es una *línea de audio*. Una línea de audio consta de uno o varios canales de datos procedentes de un único origen o un recurso del sistema. Por ejemplo, una línea de audio estéreo tiene dos canales de datos, pero se considera una sola línea de audio porque se origina desde un único origen.

La arquitectura del mezclador proporciona servicios de enrutamiento para administrar líneas de audio en un equipo. Puede usar los servicios de enrutamiento si tiene instalados los dispositivos de hardware y los controladores de software adecuados. La arquitectura del mezclador permite que varias líneas de origen de audio se asignen a una sola línea de audio de destino.

Cada línea de audio puede tener controles mezcladores asociados. Un control mezclador puede realizar cualquier número de funciones (como el volumen de control), dependiendo de las características de la línea de audio asociada.

 

 




