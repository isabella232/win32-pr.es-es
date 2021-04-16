---
description: Toda la información acerca de un archivo, incluido el tamaño, las marcas de fecha y hora, los permisos y el contenido de los datos, se almacena en las entradas de la tabla maestra de archivos (MFT) o en el espacio fuera de la MFT que se describe en las entradas de MFT.
ms.assetid: e0933846-278e-4bc8-8982-c5819c252dad
title: Tabla de archivos maestros (sistemas de archivos locales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260740c03e7b7e4ebe9c7e8ec90035431f6be649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669682"
---
# <a name="master-file-table-local-file-systems"></a>Tabla de archivos maestros (sistemas de archivos locales)

El sistema de archivos NTFS contiene un archivo denominado *tabla maestra de archivos* o MFT. Hay al menos una entrada en la MFT para cada archivo en un volumen del sistema de archivos NTFS, incluido el propio MFT. Toda la información acerca de un archivo, incluido el tamaño, las marcas de fecha y hora, los permisos y el contenido de los datos, se almacena en las entradas de MFT o en el espacio fuera de la MFT que se describe en las entradas de MFT.

A medida que se agregan archivos a un volumen del sistema de archivos NTFS, se agregan más entradas a la MFT y la MFT aumenta de tamaño. Cuando los archivos se eliminan de un volumen del sistema de archivos NTFS, sus entradas de MFT se marcan como disponibles y se pueden volver a usar. Sin embargo, el espacio en disco que se ha asignado para estas entradas no se reasigna y el tamaño de la MFT no disminuye.

El sistema de archivos NTFS Reserva espacio para que la MFT mantenga el MFT lo más contiguo posible a medida que crezca. El espacio reservado por el sistema de archivos NTFS para la MFT en cada volumen se denomina zona MFT. También se asigna espacio para archivos y directorios desde este espacio, pero solo después de que se haya asignado todo el espacio de volumen fuera de la zona MFT.

En función del tamaño de archivo medio y de otras variables, la zona MFT reservada o el espacio sin reservar del disco se pueden asignar primero a medida que el disco se llena de la capacidad. Los volúmenes con un número pequeño de archivos relativamente grandes asignarán el espacio sin reservar primero, mientras que los volúmenes con un gran número de archivos relativamente pequeños asignan primero la zona MFT. En cualquier caso, la fragmentación de la MFT comienza a tener lugar cuando una región u otra se asigna por completo. Si el espacio sin reservar se asigna por completo, el espacio de los archivos de usuario y directorios se asignará desde la zona MFT. Si la zona MFT está completamente asignada, se asignará espacio para las nuevas entradas MFT desde el espacio sin reservar.

El propio MFT se puede desfragmentar. Para reducir la posibilidad de que la zona MFT se asigne por completo antes de que se complete el proceso de desfragmentación, deje todo el espacio al principio de la zona MFT como sea posible antes de desfragmentar el volumen. Si la zona MFT se asigna por completo antes de que se complete la desfragmentación, debe haber espacio sin asignar fuera de la zona MFT.

El sistema calcula y reserva la zona MFT predeterminada cuando monta el volumen y se basa en el tamaño del volumen. Puede aumentar la zona MFT por medio de la entrada del registro que se detalla en el [artículo 174619 de Microsoft Knowledge Base](https://support.microsoft.com/kb/174619), pero no puede hacer que la zona MFT predeterminada sea menor que la que se calcula. Al aumentar la zona MFT no se reduce el espacio en disco que los usuarios pueden usar para los archivos de datos.

Para determinar el tamaño actual de la MFT, analice la unidad del sistema de archivos NTFS con el Desfragmentador de disco y haga clic en el botón **Ver informe** . Se mostrarán las estadísticas de la unidad, incluido el tamaño actual de la MFT y el número de fragmentos. También puede obtener el tamaño de la MFT con el código de control de [**\_ \_ \_ \_ datos de volumen NTFS Get**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data) .

 

 
