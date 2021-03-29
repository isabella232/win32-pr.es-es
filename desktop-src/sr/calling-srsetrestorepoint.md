---
title: Llamando a SRSetRestorePoint
description: Una aplicación puede crear un punto de restauración antes de que se produzca un cambio significativo en el sistema, como una instalación, desinstalación o actualización de características.
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b877c4fe73bcedad363bb4c9cc770a9638550dbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778517"
---
# <a name="calling-srsetrestorepoint"></a>Llamando a SRSetRestorePoint

Una aplicación puede crear un punto de restauración antes de que se produzca un cambio significativo en el sistema, como una instalación, desinstalación o actualización de características.

Los instaladores deben crear un punto de restauración justo antes de la instalación mediante una llamada a la función [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) con el miembro **dwEventType** de la estructura [**RESTOREPOINTINFO**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) establecida para comenzar el \_ cambio del sistema \_ . Para notificar a la restauración del sistema que la instalación se ha completado, llame a **SRSetRestorePoint** con **DWEVENTTYPE** establecido en finalizar el \_ cambio del sistema \_ .

Si el usuario cancela la instalación de la aplicación, el instalador puede quitar el punto de restauración que creó cuando comenzó la instalación. Quitar el punto de restauración es opcional y puede impedir que el usuario se recupere de cambios accidentales realizados por el instalador durante la cancelación. Si el instalador va a quitar un punto de restauración, puede llamar a la función [**SRRemoveRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) o llamar a [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) con **dwRestorePointType** establecido en operación cancelada \_ , **dwEventType** establecer en end \_ System \_ Change y **LlSequenceNumber** establecido en el valor devuelto por la llamada inicial a **SRSetRestorePoint**.

**Windows 8:  **

Una nueva clave del registro permite a los desarrolladores de aplicaciones cambiar la frecuencia de creación de puntos de restauración.

Las aplicaciones deben crear esta clave para usarla, ya que no existirá en el sistema. De forma predeterminada, se aplicará lo siguiente si la clave no existe. Si una aplicación llama a la función **SRSetRestorePoint** para crear un punto de restauración, Windows omite la creación de este nuevo punto de restauración si se ha creado algún punto de restauración en las últimas 24 horas. Restaurar sistema establece el miembro **IISequenceNumber** de la estructura [**STATEMGRSTATUS**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus) en el número de secuencia del punto de restauración creado anteriormente en el día y establece el valor del miembro **nStatus** en **error \_**. La función **SRSetRestorePoint** devuelve **true**.

Los desarrolladores pueden escribir aplicaciones que creen el valor **DWORD** **SystemRestorePointCreationFrequency** en la clave del registro **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. El valor de esta clave del registro puede cambiar la frecuencia de creación de puntos de restauración. El valor de esta clave del registro puede cambiar la frecuencia de creación de puntos de restauración.

Si la aplicación llama a **SRSetRestorePoint** para crear un punto de restauración y el valor de la clave del registro es 0, Restaurar sistema no omite la creación del nuevo punto de restauración.

Si la aplicación llama a **SRSetRestorePoint** para crear un punto de restauración y el valor de la clave del registro es el entero n, Restaurar sistema omite la creación de un nuevo punto de restauración si se crearon puntos de restauración en los N minutos anteriores.

**Windows 8:  **

La restauración del sistema que se ejecuta en Windows 8 supervisa los archivos del volumen de arranque que solo son relevantes para restaurar el sistema. Es posible que se eliminen las instantáneas del volumen de arranque creado por la restauración del sistema en Windows 8 Si la instantánea se expone posteriormente en una versión anterior de Windows. Tenga en cuenta que, aunque solo hay un volumen del sistema, hay un volumen de arranque para cada sistema operativo en un sistema de arranque múltiple.

Los desarrolladores pueden escribir aplicaciones que creen el valor **DWORD** **ScopeSnapshots** en la clave del registro **HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**. Si el valor de la clave del registro es 0, Restaurar sistema crea instantáneas del volumen de arranque de la misma manera que en versiones anteriores de Windows. Si se elimina este valor, la restauración del sistema que se ejecuta en Windows 8 reanuda la creación de instantáneas que supervisen los archivos del volumen de arranque que solo son relevantes para restaurar el sistema.

Para obtener un ejemplo, vea [usar Restaurar sistema](using-system-restore.md).

 

 




