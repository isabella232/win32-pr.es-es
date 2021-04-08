---
title: Arranque de archivos de imagen de Windows (WimBoot)
description: Arranque de archivos de imagen de Windows (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "103797133"
---
# <a name="windows-image-file-boot-wimboot"></a>Arranque de archivos de imagen de Windows (WimBoot)

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8.1  

## <a name="description"></a>Descripción

WimBoot es una forma alternativa para que los OEM implementen Windows. Una implementación de WimBoot inicia y ejecuta Windows directamente desde un archivo de imagen de Windows comprimido (WIM). Este archivo WIM es inmutable y el acceso a él lo administra un nuevo controlador de filtro del sistema de archivos (WoF.sys).

El resultado es una reducción significativa en el espacio en disco necesario para instalar Windows.

## <a name="manifestations"></a>Manifestaciones

La mayoría de las aplicaciones deben no verse afectadas por WimBoot. Solo pueden verse afectadas las aplicaciones que accedan a archivos del sistema o que desbloqueen archivos del sistema o archivos previamente cargados para el acceso de escritura. Dado que el WIM es inmutable, las actualizaciones de este (es decir, los archivos del sistema o cargados previamente) simplemente se almacenan en la partición C: \\ .

Si una aplicación tiene acceso de escritura desbloqueada para todos los archivos del sistema y los archivos cargados previamente, el ahorro que WimBoot entrega se perdería por completo, ya que todos estos archivos se descomprimen y se colocan en el volumen C: \\ .

Además, las aplicaciones de copia de seguridad y restauración deben tener en cuenta las implementaciones de WimBoot, ya que el WIM está presente en una partición independiente. es decir, en la copia de seguridad, se \\ deben guardar las particiones C: y Wim y ambas deben restaurarse juntas.

## <a name="solution"></a>Solución

Se introdujeron nuevas API que permiten a las aplicaciones consultar directamente si un volumen o un archivo determinado están respaldados por un WIM. Esta información permite a las aplicaciones tomar decisiones adecuadas, como abrir estos archivos solo para el acceso de lectura o identificar los volúmenes o las particiones que se deben incluir en la copia de seguridad y la restauración.

## <a name="compatibility-performance-reliability-or-usability-tests"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Los desarrolladores de aplicaciones deben probar su software y sus escenarios correspondientes en un sistema WimBoot, especialmente si estas aplicaciones tienen acceso a archivos del sistema o cargados previamente. Se debe prestar especial atención a una reducción significativa del espacio en disco disponible una vez completado un escenario.

 

 




