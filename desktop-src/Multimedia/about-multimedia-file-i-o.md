---
title: Acerca de la E/S de archivos multimedia
description: Acerca de la E/S de archivos multimedia
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows multimedia, E/S de archivos
- multimedia, E/S de archivos
- entrada multimedia, E/S de archivo
- E/S de archivos multimedia, acerca de
- E/S de archivo, acerca de
- entrada y salida (E/S), acerca de
- E/S (entrada y salida), acerca de
- E/S básica
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- E/S de RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584b736ba41fb0ea7dd5f3e6411e1783964db21a9819fbb98364708196dc2943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526645"
---
# <a name="about-multimedia-file-io"></a>Acerca de la E/S de archivos multimedia

La mayoría de las aplicaciones multimedia requieren entrada y salida de archivos (E/S), es decir, la capacidad de crear, leer y escribir archivos de disco. Los servicios de E/S de archivos multimedia proporcionan E/S de archivos almacenados en búfer y no almacenados en búfer y compatibilidad con archivos RIFF. Los servicios son extensibles con procedimientos de E/S personalizados que se pueden compartir entre las aplicaciones.

La mayoría de las aplicaciones solo necesitan los servicios básicos de E/S de archivos y los servicios de E/S de archivos RIFF. Las aplicaciones sensibles al rendimiento de E/S de archivos, como las aplicaciones que transmiten datos desde un disco compacto en tiempo real, pueden optimizar el rendimiento mediante el uso de servicios para acceder directamente al búfer de E/S de archivo. Las aplicaciones que acceden a sistemas de almacenamiento personalizados, como archivos de archivos y bases de datos, pueden proporcionar su propio procedimiento de E/S que lee y escribe elementos del sistema de almacenamiento.

 

 




