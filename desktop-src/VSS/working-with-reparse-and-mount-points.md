---
description: El procesamiento de uno de los conjuntos de archivos de un componente puede requerir que un solicitante atraviese un árbol de directorio de forma recursiva, lo que puede requerir que el solicitante controle las carpetas montadas y los puntos de rean aproximado (como vínculos) que apunten a datos que no están en el volumen actual.
ms.assetid: d0e08598-a8a2-489b-9cb2-e989bed1ce53
title: Trabajar con carpetas montadas y puntos de reanción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1162d1d7da5869f588ae61d9235ec3d5827265c5eb9deaa23c38b8b9e85db68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905065"
---
# <a name="working-with-mounted-folders-and-reparse-points"></a>Trabajar con carpetas montadas y puntos de reanción

El procesamiento de uno de los conjuntos de archivos de un componente puede requerir que un solicitante atraviese un árbol de directorio de forma recursiva, lo que puede requerir que el solicitante controle las carpetas montadas y los puntos de rean aproximado (como vínculos) que apunten a datos que no están en el volumen actual.

Se espera que los solicitantes sigan las carpetas montadas y los puntos de reanquiso al recorrer un árbol de directorios, y VSS tiene directrices bien definidas para controlarlas para las operaciones de copia de seguridad y restauración.

Para ilustrar estas directrices, considere el ejemplo siguiente:

-   El volumen \\ \\ ? \\ El volumen{GUID \_ 1} tiene la letra de unidad C: \\ .
-   Un conjunto de archivos tiene una ruta de acceso de C: \\ WriterData.
-   El conjunto de archivos \* usa una especificación de archivo .dat.
-   La recursividad del conjunto de archivos se establece en **TRUE.**
-   El directorio C: \\ WriterData se encuentra en el volumen \\ \\ ? \\ Volumen{GUID \_ 1}.
-   El directorio C: \\ WriterData \\ Archive es una carpeta montada.
-   El volumen \\ \\ ? \\ El volumen{GUID \_ 2} está asociado a la carpeta montada C: \\ WriterData \\ Archive.

## <a name="handling-mounted-folders-and-reparse-points-during-backup"></a>Control de carpetas montadas y puntos de reanción durante la copia de seguridad

Las reglas básicas para controlar las carpetas montadas y los puntos de reanualidad en VSS al realizar una copia de seguridad recursiva se pueden resumir de la siguiente manera:

-   Las rutas de acceso se siguen entre carpetas montadas y puntos de rean aproximado.
-   Si una carpeta montada o un punto de reanual apunta a un volumen, ese volumen debe copiarse en la sombra.
-   Si un volumen contiene carpetas montadas o puntos de rean aproximado, aparecerán en la instantánea del volumen.
-   Los datos que se encuentra bajo la carpeta montada o el punto de rean aproximado se capturan en la instantánea del volumen al que apunta la carpeta montada o el punto de análisis.

Para ilustrar el uso del ejemplo anterior, dado que la marca recursiva está establecida, el solicitante debe examinar todos los datos en C: WriterData Archive y a \\ \\ continuación.

El solicitante debe agregar el volumen con la letra de unidad C: \\ ( \\ \\ ? \\ Volumen{GUID 1}) y el volumen asociado a la carpeta \_ montada C: \\ WriterData \\ Archive ( \\ \\ ? \\ Volumen{GUID \_ 2}) al conjunto de instantáneas mediante [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

La carpeta montada C: \\ WriterData \\ Archive aparece en la instantánea del volumen \\ \\ ? \\ Volumen{GUID \_ 1}, que tiene un objeto de dispositivo denominado deviceObject1.

Sin embargo, VSS no copiará ningún dato en esa carpeta montada (datos en \\ \\ ? \\ Volumen{GUID 2}) a la instantánea a la que hace \_ referencia deviceObject1. En su lugar, los datos se capturan en la instantánea de \\ \\ ? \\ Volumen{GUID \_ 2}, que tiene un objeto de dispositivo denominado deviceObject2.

Por lo tanto, un solicitante que hace una copia de seguridad de archivos copiados en la sombra en C: WriterData usará una ruta de acceso de deviceObject1 WriterData para buscar archivos que coincidan con \\ \\ C: \\ WriterData \\ \* .dat.

Para hacer una copia de seguridad de los archivos copiados en la sombra en C: WriterData Archive, el solicitante usará una ruta de \\ \\ acceso de deviceObject2 (porque el directorio raíz de \\ \\ ? \\ El volumen{GUID 2} se asoció a la carpeta montada C: Writer Archive) para buscar archivos que coincidan con \_ \\ \\ C: \\ WriterData \\ Archive \\ \* .dat.

Tenga en cuenta que un punto de reanual se controla de la misma manera que una carpeta montada. El punto de rean aproximado aparece en la instantánea del primer volumen. Los datos bajo el punto de análisis aparecen en la instantánea del segundo volumen.

Durante la copia de seguridad, los solicitantes deben almacenar información sobre las carpetas montadas y los volúmenes asociados a ellas, así como los puntos de análisis y sus destinos para asegurarse de que todos los datos se copian y restauran correctamente.

## <a name="handling-mount-and-reparse-points-during-restore"></a>Control de los puntos de montaje y reanción durante la restauración

Al restaurar archivos, el solicitante debe seguir instrucciones algo diferentes de las que [](vssgloss-a.md) se usaron durante la copia de seguridad (omitiendo problemas como la asignación de ubicación alternativa y la nueva [*ubicación de destino):*](vssgloss-n.md)

-   Como antes, si se requiere recursividad, las rutas de acceso se siguen entre carpetas montadas y puntos de rean aproximado.
-   Las carpetas montadas se restaurarán.
-   Las ubicaciones de restauración de las carpetas montadas y los puntos de rean aproximado son las que determinan sus rutas de acceso originales.

Si los nombres de volumen persisten entre la copia de seguridad y la restauración (es decir, no vuelve a crear los volúmenes), las carpetas montadas restauradas y los puntos de rean aproximado deben apuntar a los volúmenes correctos.

Por lo tanto, en el ejemplo descrito anteriormente, si la carpeta montada C: WriterData Archive se restauró \\ \\ en ( \\ \\ ? \\ Volumen{GUID \_ 1}) y el volumen asociado previamente a él se restauró en ( \\ \\ ? \\ Volumen{GUID \_ 2}), los archivos restaurados y la estructura de archivos serían correctos y coherentes.

Puede ocurrir que los datos se restauró en un sistema donde cambiaron los nombres de volumen. Esto podría deberse a bloqueos de disco, donde es posible que tenga que realizar una recuperación manual del sistema y volver a crear volúmenes. En este tipo de situación, las carpetas montadas y los puntos de rean url ya no serán válidos después de la restauración. Para volver a crear los archivos y la estructura de archivos en el volumen restaurado, será necesario eliminar las carpetas montadas restauradas y los puntos de análisis y volver a crearlos en el disco. Es decisión de la aplicación de copia de seguridad decidir si es adecuado.

Tenga en cuenta que es posible que el destino de restauración de una carpeta montada ya esté ocupado. Por ejemplo, C: \\ WriterData \\ Archive podría contener ya algunos archivos. Es decisión de la aplicación de copia de seguridad decidir cómo controlar esta situación.

 

 



