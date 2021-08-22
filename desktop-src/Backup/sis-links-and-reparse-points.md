---
title: Vínculos de SIS y puntos de reanlabaciones
description: SIS es un controlador de filtro NTFS que reemplaza los archivos duplicados por vínculos de copia en escritura (denominados vínculos SIS) que apuntan a un único archivo de respaldo, lo que reduce la sobrecarga de disco y caché de esos archivos.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- copias de seguridad de puntos de reanción
- Copia de seguridad de almacén de instancia única (SIS), vínculos de SIS
- copia de seguridad de almacén de instancia única (SIS), puntos de rean aproximado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f89901df6ce1fea1635d4250f2884ec9baf68fb1552766564909486c8ed00a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588865"
---
# <a name="sis-links-and-reparse-points"></a>Vínculos de SIS y puntos de reanlabaciones

SIS es un controlador de filtro NTFS que reemplaza los archivos duplicados por vínculos de copia en escritura (denominados vínculos SIS) que apuntan a un único archivo de respaldo, lo que reduce la sobrecarga de disco y caché de esos archivos. Este archivo de respaldo se encuentra en un [almacén común.](the-sis-common-store-and-common-store-files.md) La implementación de la arquitectura de SIS usa puntos [de reanlabación](/windows/desktop/FileIO/reparse-points) que contienen información sobre los vínculos de SIS.

Los vínculos DE SIS se implementan como archivos dispersos, normalmente con la mayoría de los intervalos del archivo sin asignar y un punto de análisis. La estructura y el contenido de un punto de reanción son opacos para las aplicaciones de copia de seguridad y restauración. Sin embargo, las aplicaciones envían y recuperan los datos dentro de estos puntos de rean aproximado hacia y desde las funciones de API de SIS que procesan la información en ellas. La información de un punto de análisis hace referencia a un único archivo de respaldo que contiene los datos reales del archivo. Este archivo de respaldo se denomina [archivo de almacenamiento](the-sis-common-store-and-common-store-files.md)común y existe en el almacén común.

Al restaurar un vínculo de SIS, la aplicación de restauración debe realizar los pasos siguientes:

1.  Determine el archivo de almacenamiento común o los archivos a los que apunta el vínculo de SIS.
2.  Si el archivo o los archivos no existen en el almacén común, restaure el archivo o los archivos junto con el vínculo SIS.
3.  Si el vínculo de SIS apunta a un archivo de almacenamiento común o a archivos que existen en el disco, restaure solo el vínculo SIS. Recuerde que los datos de los archivos de almacenamiento común nunca cambian, por lo que si un archivo de almacenamiento común determinado todavía está en el disco en tiempo de restauración, tiene el mismo contenido que cuando se hizo una copia de seguridad y no es necesario sobrescribirlo.

La única sobrecarga adicional necesaria para las copias de seguridad asistidas por SIS es que la aplicación de copia de seguridad debe realizar una copia de seguridad del vínculo de SIS y los datos asociados a los archivos de respaldo. Todas las operaciones de copia de seguridad y restauración de SIS son locales en un volumen específico.

 

 