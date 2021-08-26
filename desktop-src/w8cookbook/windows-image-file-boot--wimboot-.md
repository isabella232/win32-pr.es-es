---
title: Windows Arranque de archivo de imagen (WimBoot)
description: Windows Arranque de archivo de imagen (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687a230188c3b13317d8176d8209cf5e38026c3b6f161be7ffe0c2ed760976ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932125"
---
# <a name="windows-image-file-boot-wimboot"></a>Windows Arranque de archivo de imagen (WimBoot)

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8.1  

## <a name="description"></a>Descripción

WimBoot es una manera alternativa para que los OEM implementen Windows. Una implementación de WimBoot se inicia y Windows directamente desde un archivo Windows imagen (WIM) comprimido. Este archivo WIM es inmutable y el acceso a él se administra mediante un nuevo controlador de filtro del sistema de archivos (WoF.sys).

El resultado es una reducción significativa del espacio en disco necesario para instalar Windows.

## <a name="manifestations"></a>Manifestaciones

La mayoría de las aplicaciones no deben estar afectadas por WimBoot. Solo las aplicaciones que acceden y desbloquean archivos del sistema o archivos cargados previamente para el acceso de escritura pueden verse afectadas. Puesto que WIM es inmutable, las actualizaciones de él (es decir, archivos cargados previamente o del sistema) simplemente se almacenan en la partición \\ C:.

Si una aplicación desbloquea el acceso de escritura para todos los archivos precargados y del sistema con el respaldo de WIM, el ahorro que proporciona WimBoot se perdería por completo, ya que todos estos archivos se descomprimirán y colocarían en el volumen \\ C:.

Además, las aplicaciones de copia de seguridad y restauración deben tener en cuenta las implementaciones de WimBoot, ya que wim está presente en una partición independiente. Es decir, en la copia de seguridad, se deben guardar las particiones C: y WIM y ambas \\ deben restaurarse juntas.

## <a name="solution"></a>Solución

Se introdujeron nuevas API que permiten a las aplicaciones consultar directamente si un volumen o archivo determinado está a favor de un WIM. Esta información permite a las aplicaciones tomar las decisiones adecuadas, como abrir estos archivos solo para el acceso de lectura o identificar los volúmenes o particiones de los que es necesario realizar una copia de seguridad y restaurarlos juntos.

## <a name="compatibility-performance-reliability-or-usability-tests"></a>Pruebas de compatibilidad, rendimiento, confiabilidad o facilidad de uso

Los desarrolladores de aplicaciones deben probar su software y sus escenarios correspondientes en un sistema WimBoot, especialmente si estas aplicaciones acceden al sistema o a archivos cargados previamente. Se debe prestar especial atención a una reducción significativa del espacio disponible en disco una vez completado un escenario.

 

 




