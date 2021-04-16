---
description: El procesamiento de uno de los conjuntos de archivos de un componente puede requerir que un solicitante atraviese un árbol de directorios de forma recursiva, lo que puede requerir que el solicitante controle las carpetas montadas y los puntos de reanálisis (como los vínculos) que apuntan a datos que no están en el volumen actual.
ms.assetid: d0e08598-a8a2-489b-9cb2-e989bed1ce53
title: Trabajar con carpetas montadas y puntos de análisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a7aa88f39361f788f9aac882b4f9d337fd6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696429"
---
# <a name="working-with-mounted-folders-and-reparse-points"></a>Trabajar con carpetas montadas y puntos de análisis

El procesamiento de uno de los conjuntos de archivos de un componente puede requerir que un solicitante atraviese un árbol de directorios de forma recursiva, lo que puede requerir que el solicitante controle las carpetas montadas y los puntos de reanálisis (como los vínculos) que apuntan a datos que no están en el volumen actual.

Se espera que los solicitantes sigan las carpetas montadas y los puntos de análisis al atravesar un árbol de directorios, y VSS tiene directrices bien definidas para controlarlas en operaciones de copia de seguridad y restauración.

Para ilustrar estas instrucciones, considere el ejemplo siguiente:

-   ¿El volumen \\ \\ ? \\ El volumen {GUID \_ 1} tiene la letra de unidad C: \\ .
-   Un conjunto de archivos tiene una ruta de acceso de C: \\ WriterData.
-   Un archivo Specification \* . dat lo utiliza el conjunto de archivos.
-   La recursividad del conjunto de archivos se establece en **true**.
-   ¿El directorio C: \\ WriterData se encuentra en el volumen \\ \\ ? \\ Volumen {GUID \_ 1}.
-   El directorio C: \\ WriterData \\ Archive es una carpeta montada.
-   ¿El volumen \\ \\ ? \\ El volumen {GUID \_ 2} está asociado a la carpeta montada C: \\ WriterData \\ Archive.

## <a name="handling-mounted-folders-and-reparse-points-during-backup"></a>Administrar carpetas montadas y puntos de análisis durante la copia de seguridad

Las reglas básicas para controlar las carpetas montadas y los puntos de análisis en VSS al realizar una copia de seguridad recursiva se pueden resumir de la manera siguiente:

-   Las rutas de acceso se siguen entre las carpetas montadas y los puntos de reanálisis.
-   Si una carpeta montada o un punto de análisis apunta a un volumen, se debe realizar una instantánea de ese volumen.
-   Si un volumen contiene carpetas montadas o puntos de reanálisis, aparecerán en la instantánea del volumen.
-   Los datos que se encuentra bajo la carpeta montada o el punto de reanálisis se capturan en la instantánea del volumen al que apunta la carpeta montada o el punto de reanálisis.

Para ilustrar el uso del ejemplo anterior, dado que se establece la marca recursiva, el solicitante debe examinar todos los datos en C: \\ WriterData \\ Archive y a continuación.

El solicitante debe agregar el volumen con la letra de unidad C: \\ ( \\ \\ ? \\ Volumen {GUID \_ 1}) y el volumen asociado a la carpeta montada C: \\ WriterData \\ Archive ( \\ \\ ? \\ Volumen {GUID \_ 2}) al conjunto de instantáneas mediante [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

La carpeta montada C: \\ WriterData \\ Archive aparece en la instantánea del volumen \\ \\ \\ . Volumen {GUID \_ 1}, que tiene un objeto de dispositivo denominado deviceObject1.

Sin embargo, VSS no copiará ningún dato en esa carpeta montada (datos en \\ \\ ? \\ Volumen {GUID \_ 2}) a la instantánea a la que hace referencia deviceObject1. En su lugar, los datos se capturan en la instantánea de \\ \\ ? \\ Volumen {GUID \_ 2}, que tiene un objeto de dispositivo denominado deviceObject2.

Por lo tanto, un solicitante que realice copias de seguridad de archivos de copia sombra bajo C: \\ WriterData usará una ruta de acceso de deviceObject1 \\ WriterData para buscar archivos que coincidan con c: \\ WriterData \\ \* . dat.

Para hacer una copia de seguridad de los archivos de copia sombra en C: \\ WriterData \\ Archive, el solicitante usará una ruta de acceso de deviceObject2 (porque el directorio raíz de \\ \\ ? \\ El volumen {GUID \_ 2} se asoció con la carpeta montada c: \\ Writer \\ Archive) para buscar archivos que coincidan con c: \\ WriterData \\ Archive \\ \* . dat.

Tenga en cuenta que un punto de análisis se administra de la misma manera que una carpeta montada. El punto de reanálisis aparece en la instantánea del primer volumen. Los datos del punto de reanálisis aparecen en la instantánea del segundo volumen.

Durante la copia de seguridad, los solicitantes deben almacenar información sobre las carpetas montadas y los volúmenes asociados a ellas, así como los puntos de reanálisis y sus destinos para asegurarse de que se realiza una copia de seguridad de todos los datos y se restauran correctamente.

## <a name="handling-mount-and-reparse-points-during-restore"></a>Control de los puntos de montaje y análisis durante la restauración

Al restaurar archivos, el solicitante debe seguir las instrucciones de forma ligeramente diferente de las que se usaron durante la copia de seguridad (omitiendo problemas como la [*asignación de ubicación alternativa*](vssgloss-a.md) y la [*nueva ubicación de destino*](vssgloss-n.md)):

-   Como antes, si se requiere la recursividad, se siguen las rutas de acceso a través de las carpetas montadas y los puntos de reanálisis.
-   Las carpetas montadas se van a restaurar.
-   Las ubicaciones de restauración de las carpetas montadas y los puntos de reanálisis son las que determinan sus rutas de acceso originales.

Si los nombres de los volúmenes persisten entre la copia de seguridad y la restauración, es decir, no vuelve a crear los volúmenes, las carpetas montadas y los puntos de análisis que se restauran deben apuntar a los volúmenes correctos.

Por lo tanto, en el ejemplo descrito anteriormente, si la carpeta montada C: \\ WriterData \\ Archive se restauró en ( \\ \\ ? \\ \_Se restauró el volumen {GUID 1}) y el volumen asociado anteriormente a este ( \\ \\ ? \\ Volumen {GUID \_ 2}), los archivos y la estructura de archivos restaurados serían correctos y coherentes.

Puede suceder que los datos se restauren en un sistema en el que los nombres de los volúmenes hayan cambiado. Esto puede deberse a bloqueos de disco, en los que es posible que necesite realizar una recuperación manual del sistema y volver a crear los volúmenes. En este tipo de situación, las carpetas montadas y los puntos de análisis dejarán de ser válidos después de la restauración. Para volver a crear los archivos y la estructura de archivos en el volumen restaurado, será necesario eliminar las carpetas montadas restauradas y los puntos de análisis y volver a crearlos en el disco. Depende de la aplicación de copia de seguridad decidir si esto es adecuado.

Tenga en cuenta que es posible que el destino de restauración de una carpeta montada ya esté ocupado. Por ejemplo, \\ puede que el archivo C: WriterData \\ ya contenga algunos archivos. Depende de la aplicación de copia de seguridad decidir cómo tratar esta situación.

 

 



