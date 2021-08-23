---
description: Toda la información sobre un archivo, incluidos su tamaño, marcas de hora y fecha, permisos y contenido de datos, se almacena en entradas de la tabla de archivos maestras (MFT) o en un espacio fuera de MFT descrito por las entradas de MFT.
ms.assetid: e0933846-278e-4bc8-8982-c5819c252dad
title: Tabla de archivos maestra (sistemas de archivos locales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fefec19906e6e2e2c67bbcabf8bd891ccc032b7e8d0882a3622011c324d11c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525645"
---
# <a name="master-file-table-local-file-systems"></a>Tabla de archivos maestra (sistemas de archivos locales)

El sistema de archivos NTFS contiene un archivo denominado tabla *de archivos maestra* o MFT. Hay al menos una entrada en MFT para cada archivo de un volumen del sistema de archivos NTFS, incluido el propio MFT. Toda la información sobre un archivo, incluidos su tamaño, marcas de hora y fecha, permisos y contenido de datos, se almacena en entradas de MFT o en un espacio fuera de MFT descrito por las entradas de MFT.

A medida que se agregan archivos a un volumen del sistema de archivos NTFS, se agregan más entradas a MFT y el tamaño de MFT aumenta. Cuando se eliminan archivos de un volumen del sistema de archivos NTFS, sus entradas de MFT se marcan como gratuitas y se pueden reutilizar. Sin embargo, el espacio en disco que se ha asignado para estas entradas no se reasigna y el tamaño de MFT no disminuye.

El sistema de archivos NTFS reserva espacio para que MFT mantenga el MFT lo más contiguo posible a medida que crece. El espacio reservado por el sistema de archivos NTFS para MFT en cada volumen se denomina zona MFT. También se asigna espacio para archivos y directorios desde este espacio, pero solo después de que se haya asignado todo el espacio de volumen fuera de la zona MFT.

Según el tamaño medio del archivo y otras variables, la zona reservada de MFT o el espacio no reservado en el disco se pueden asignar primero a medida que el disco se llena de capacidad. Los volúmenes con un pequeño número de archivos relativamente grandes asignarán primero el espacio sin reserva, mientras que los volúmenes con un gran número de archivos relativamente pequeños asignan primero la zona MFT. En cualquier caso, la fragmentación de MFT comienza a tener lugar cuando una región u otra se asignan por completo. Si el espacio sin reserva está completamente asignado, se asignará espacio para los archivos y directorios de usuario desde la zona MFT. Si la zona MFT está completamente asignada, se asignará espacio para las nuevas entradas de MFT desde el espacio sin reserva.

El propio MFT se puede desfragmentar. Para reducir la posibilidad de que la zona MFT se asigne por completo antes de que se complete el proceso de desfragmentación, deje tanto espacio al principio de la zona MFT como sea posible antes de desfragmentar el volumen. Si la zona MFT se asigna completamente antes de que se complete la desfragmentación, debe haber espacio sin asignar fuera de la zona MFT.

El sistema calcula y reserva la zona MFT predeterminada cuando monta el volumen y se basa en el tamaño del volumen. Puede aumentar la zona MFT mediante la entrada del Registro que se detalla en el artículo 174619 de [Microsoft Knowledge Base](https://support.microsoft.com/kb/174619), pero no puede hacer que la zona MFT predeterminada sea menor que la que se calcula. El aumento de la zona MFT no reduce el espacio en disco que los usuarios pueden usar para los archivos de datos.

Para determinar el tamaño actual de MFT, analice la unidad del sistema de archivos NTFS con desfragmentador de disco y, a continuación, haga clic en el **botón Ver** informe. Se mostrarán las estadísticas de unidad, incluido el tamaño actual de MFT y el número de fragmentos. También puede obtener el tamaño de MFT mediante el código de control [**FSCTL \_ GET NTFS \_ VOLUME \_ \_ DATA.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)

 

 
