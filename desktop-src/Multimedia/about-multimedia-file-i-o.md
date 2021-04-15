---
title: Acerca de la e/s de archivos multimedia
description: Acerca de la e/s de archivos multimedia
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows multimedia, e/s de archivos
- multimedia, e/s de archivos
- entrada multimedia, e/s de archivos
- e/s de archivos multimedia, acerca de
- e/s de archivos, acerca de
- entrada y salida (e/s), acerca de
- E/s (entrada y salida), acerca de
- e/s básicas
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- RIFF E/S
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676163"
---
# <a name="about-multimedia-file-io"></a>Acerca de la e/s de archivos multimedia

La mayoría de las aplicaciones multimedia requieren entrada y salida (e/s) de archivo, es decir, la capacidad de crear, leer y escribir archivos de disco. Los servicios de e/s de archivos multimedia proporcionan e/s de archivos en búfer y no almacenada en búfer y admiten archivos RIFF. Los servicios son extensibles con procedimientos de e/s personalizados que se pueden compartir entre aplicaciones.

La mayoría de las aplicaciones solo necesitan los servicios básicos de e/s de archivos y los servicios de e/s de archivos RIFF. Las aplicaciones sensibles al rendimiento de e/s de archivos, como las aplicaciones que transmiten datos de un disco compacto en tiempo real, pueden optimizar el rendimiento mediante el uso de servicios para acceder directamente al búfer de e/s de archivos. Las aplicaciones que tienen acceso a sistemas de almacenamiento personalizados, como archivos de archivos y bases de datos, pueden proporcionar su propio procedimiento de e/s que lee y escribe elementos del sistema de almacenamiento.

 

 




