---
title: Vínculos de SIS y puntos de análisis
description: SIS es un controlador de filtro NTFS que reemplaza los archivos duplicados por vínculos de copia en escritura (denominados vínculos de SIS) que apuntan a un solo archivo de copia de seguridad, lo que reduce el disco y la sobrecarga de almacenamiento en caché de esos archivos.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- Copia de seguridad de puntos de análisis
- Copia de seguridad de almacenamiento de instancia única (SIS), vínculos de SIS
- Copia de seguridad de almacenamiento de instancia única (SIS), puntos de análisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4987e7c64a83e7d0b02ed91899a182616be7943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149504"
---
# <a name="sis-links-and-reparse-points"></a>Vínculos de SIS y puntos de análisis

SIS es un controlador de filtro NTFS que reemplaza los archivos duplicados por vínculos de copia en escritura (denominados vínculos de SIS) que apuntan a un solo archivo de copia de seguridad, lo que reduce el disco y la sobrecarga de almacenamiento en caché de esos archivos. Este archivo de copia de seguridad se encuentra en un [almacén común](the-sis-common-store-and-common-store-files.md). La implementación de la arquitectura de SIS hace uso de [puntos de reanálisis](/windows/desktop/FileIO/reparse-points) que contienen información sobre los vínculos de SIS.

Los vínculos de SIS se implementan como archivos dispersos, normalmente con la mayoría de los intervalos del archivo sin asignar y un punto de reanálisis. La estructura y el contenido de un punto de análisis es opaco para las aplicaciones de copia de seguridad y restauración; sin embargo, las aplicaciones envían y recuperan los datos de estos puntos de análisis a y desde las funciones de la API de SIS que procesan la información que contiene. La información de un punto de análisis hace referencia a un único archivo de copia de seguridad que contiene los datos de archivos reales. Este archivo de copia de seguridad se denomina [archivo de almacenamiento común](the-sis-common-store-and-common-store-files.md)y existe en el almacén común.

Al restaurar un vínculo de SIS, la aplicación de restauración debe realizar los siguientes pasos:

1.  Determine el archivo o los archivos de almacenamiento común a los que apunta el vínculo de SIS.
2.  Si el archivo o los archivos no existen en el almacén común, restaure el archivo o los archivos junto con el vínculo SIS.
3.  Si el vínculo SIS apunta a un archivo o archivos de almacenamiento común que existen en el disco, restaure solo el vínculo SIS. Recuerde que los datos de los archivos de almacenamiento común nunca cambian, por lo que si un archivo de almacenamiento común determinado todavía está en el disco en el momento de la restauración, tiene el mismo contenido que cuando se hizo una copia de seguridad y no es necesario sobrescribirlo.

La única sobrecarga adicional necesaria para las copias de seguridad asistidas por SIS es que la aplicación de copia de seguridad debe realizar copias de seguridad del vínculo SIS y de los datos asociados con los archivos de copia de seguridad. Todas las operaciones de copia de seguridad y restauración de SIS son locales para un volumen específico.

 

 