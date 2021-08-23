---
title: Llamada a SRSetRestorePoint
description: Una aplicación puede crear un punto de restauración antes de provocar un cambio significativo del sistema, como una instalación, desinstalación o actualización de características.
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ee2fc64fc74dd9ceeff4856a6a63effe0667ff2bd837d7dc8ae521172a1c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592215"
---
# <a name="calling-srsetrestorepoint"></a>Llamada a SRSetRestorePoint

Una aplicación puede crear un punto de restauración antes de provocar un cambio significativo del sistema, como una instalación, desinstalación o actualización de características.

Los instaladores deben crear un punto de restauración justo antes de la instalación llamando a la función [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) con el **miembro dwEventType** de la estructura [**RESTOREPOINTINFO**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) establecido en BEGIN \_ SYSTEM \_ CHANGE. Para notificar Restaurar sistema que se ha completado la instalación, llame a **SRSetRestorePoint** con **dwEventType** establecido en END \_ SYSTEM \_ CHANGE.

Si el usuario cancela la instalación de la aplicación, el instalador puede quitar el punto de restauración que creó cuando comenzó la instalación. La eliminación del punto de restauración es opcional y puede impedir que el usuario se recupere de los cambios involuntarias realizados por el instalador durante la cancelación. Si el instalador va a quitar un punto de restauración, puede llamar a la función [**SRRemoveRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) o llamar a [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) con **dwRestorePointType** establecido en CANCELLED OPERATION, dwEventType establecido en END SYSTEM CHANGE y llSequenceNumber establecido en el valor devuelto por la llamada inicial a \_  \_ \_ **SRSetRestorePoint.** 

**Windows 8: **

Una nueva clave del Registro permite a los desarrolladores de aplicaciones cambiar la frecuencia de creación del punto de restauración.

Las aplicaciones deben crear esta clave para usarla porque no será preexistnte en el sistema. Lo siguiente se aplicará de forma predeterminada si la clave no existe. Si una aplicación llama a la función **SRSetRestorePoint** para crear un punto de restauración, Windows omite la creación de este nuevo punto de restauración si se han creado puntos de restauración en las últimas 24 horas. Restaurar sistema establece el miembro **IISequenceNumber** de la estructura [**STATEMGRSTATUS**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus) en el número de secuencia del punto de restauración creado anteriormente en el día y establece el valor del miembro **nStatus** en **ERROR \_ SUCCESS**. La **función SRSetRestorePoint** devuelve **TRUE.**

Los desarrolladores pueden escribir aplicaciones que creen el valor **DWORD** **SystemRestorePointCreationFrequency** en la clave del Registro **HKLM \\ Software Microsoft Windows \\ NT \\ \\ CurrentVersion \\ SystemRestore**. El valor de esta clave del Registro puede cambiar la frecuencia de creación del punto de restauración. El valor de esta clave del Registro puede cambiar la frecuencia de creación del punto de restauración.

Si la aplicación llama a **SRSetRestorePoint** para crear un punto de restauración y el valor de la clave del Registro es 0, la restauración del sistema no omite la creación del nuevo punto de restauración.

Si la aplicación llama a **SRSetRestorePoint** para crear un punto de restauración y el valor de la clave del Registro es el entero N, la restauración del sistema omite la creación de un nuevo punto de restauración si se crearon puntos de restauración en los N minutos anteriores.

**Windows 8: **

Restaurar sistema se ejecuta en Windows 8 supervisa los archivos del volumen de arranque que solo son pertinentes para la restauración del sistema. Las instantáneas del volumen de arranque creado por Restaurar sistema que se ejecutan en Windows 8 pueden eliminarse si la instantánea se expone posteriormente mediante una versión anterior de Windows. Tenga en cuenta que, aunque solo hay un volumen del sistema, hay un volumen de arranque para cada sistema operativo en un sistema de varios arranques.

Los desarrolladores pueden escribir aplicaciones que creen el valor **DWORD** **ScopeSnapshots** en la clave del Registro **HKLM \\ Software Microsoft Windows \\ NT \\ \\ CurrentVersion \\ SystemRestore**. Si este valor de clave del Registro es 0, Restaurar sistema instantáneas del volumen de arranque de la misma manera que en versiones anteriores de Windows. Si se elimina este valor, Restaurar sistema en Windows 8 reanuda la creación de instantáneas que supervisan los archivos del volumen de arranque que solo son pertinentes para la restauración del sistema.

Para obtener un ejemplo, [vea Using Restaurar sistema](using-system-restore.md).

 

 




