---
title: Puntos de restauración
description: Los puntos de restauración se crean para permitir que los usuarios elijan los Estados anteriores del sistema. Cada punto de restauración contiene la información necesaria para restaurar el sistema al Estado elegido. Los puntos de restauración se crean antes de que se realicen cambios clave en el sistema.
ms.assetid: 5f68b377-4293-493e-afaf-f4414c2af1fb
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.date: 12/06/2019
manager: dcscontentpm
ms.custom: CSSTroubleshooting
ms.openlocfilehash: 6ef1aba7d1cb018bb3fa4f32d868828ef2ac4d1b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359293"
---
# <a name="restore-points"></a>Puntos de restauración

Se crean puntos de restauración para permitir que los usuarios seleccionen un estado del sistema anterior. Cada punto de restauración contiene la información necesaria para restaurar el sistema al estado seleccionado. Los puntos de restauración se crean antes de que se realicen cambios clave en el sistema.

Restaurar sistema administra automáticamente el espacio en disco asignado para los puntos de restauración. Purga los puntos de restauración más antiguos para dejar espacio a los nuevos. Restaurar sistema asigna espacio en función del tamaño del disco duro y la versión de Windows que ejecuta el equipo, tal como se muestra en la tabla siguiente.

|Versión de Windows |&nbsp;Tamaño del disco duro |Espacio de restauración del sistema |
| --- | --- | --- |
|Windows 7 y versiones posteriores | > 64 GB |Hasta el cinco por ciento del espacio total en disco o un máximo de 10 GB, lo que sea menor |
|  | &le; 64 GB |Hasta el tres por ciento del espacio total en disco |
|Windows Vista |  |Hasta un 15% del total de espacio en disco o un máximo del 30 por ciento de espacio disponible en disco, lo que sea menor |
|Windows XP | >4 GB |Hasta el 12 por ciento del espacio total en disco<br /><br />Para cambiar el límite de almacenamiento máximo en Windows XP, use el elemento **sistema** del panel de control. |
|  | \< 4 GB |Hasta 400 MB |

## <a name="event-triggered-restore-points"></a>Puntos de restauración desencadenados por eventos

Restaurar sistema crea automáticamente un punto de restauración antes de que se produzca cualquiera de los siguientes eventos:

- **Instalación** de la aplicación (se aplica solo a las aplicaciones que usan un instalador compatible con Restaurar sistema). Si la instalación de la aplicación produce problemas en el sistema, el usuario puede restaurar el sistema a un estado que preceda a la instalación.
- **Instalación de Windows Update o de actualización automática**. Windows Update (conocido anteriormente como AutoUpdate) descarga e instala automáticamente las actualizaciones de Windows. Además, proporciona a los usuarios una forma sencilla de descargar e instalar las actualizaciones de forma manual. Restaurar sistema crea un punto de restauración antes de instalar una actualización, ya sea de forma automática o manual.
- **Operación de restauración del sistema**. Restaurar sistema crea automáticamente un punto de restauración como copia de seguridad antes de que se inicie cualquier operación de restauración. Por ejemplo, supongamos que un usuario restaura accidentalmente Windows a un punto de restauración incorrecto. Para deshacer esa restauración, el usuario puede restaurar Windows a un punto de restauración anterior al primer punto de restauración. Una vez que Windows se haya restaurado a su estado inicial, el usuario podrá repetir el proceso, pero esta vez Seleccione el punto de restauración correcto.

## <a name="scheduled-restore-points"></a>Puntos de restauración programados

Los usuarios pueden configurar Restaurar sistema para crear puntos de restauración a intervalos regulares. Los usuarios también pueden crear y asignar nombres manualmente a un punto de restauración en cualquier momento desde la interfaz de usuario de restauración del sistema. Estos puntos de restauración se guardan y se comprimen, y están disponibles en la lista de puntos de restauración.

En Windows 7 y versiones posteriores, Restaurar sistema crea un punto de restauración programado solo si no se ha creado ningún otro punto de restauración en los siete días anteriores. En Windows Vista, Restaurar sistema crea un punto de control cada 24 horas si no se creó ningún otro punto de restauración en ese día. En Windows XP, Restaurar sistema crea un punto de control cada 24 horas, independientemente de otras operaciones.

## <a name="known-issue-you-cannot-restore-the-system-to-a-restore-point-after-you-install-a-windows-10-update"></a>Problema conocido: no se puede restaurar el sistema a un punto de restauración después de instalar una actualización de Windows 10

Considere el caso siguiente:

1. Instale Windows 10 en un equipo limpio.
1. Active la protección del sistema y, a continuación, cree un punto de restauración del sistema denominado "R1".
1. Instala una o varias actualizaciones de Windows 10.
1. Una vez finalizada la instalación de las actualizaciones, restaure el sistema en el punto de restauración "R1".

En este escenario, el sistema no se restaura al punto de restauración "R1". En su lugar, el equipo experimenta un error de detención (0xc000021a). Reinicie el equipo, pero el sistema no podrá volver al escritorio de Windows.

### <a name="cause"></a>Causa

Se trata de un problema conocido en Windows 10.

Durante el proceso de restauración del sistema, Windows almacena temporalmente en fases la restauración de los archivos que se están usando. Después guarda la información en el registro. Cuando se reinicia el equipo, se completa la operación almacenada provisionalmente.

En esta situación, Windows restaura los archivos de catálogo y crea fases en los archivos de controlador (. sys) que se restaurarán cuando se reinicie el equipo. Sin embargo, cuando se reinicia el equipo, Windows carga los controladores existentes antes de restaurar las versiones posteriores de los controladores. Dado que las versiones del controlador no coinciden con las versiones de los archivos de catálogo restaurados, se detiene el proceso de reinicio.

### <a name="workaround"></a>Solución alternativa

**Para recuperarse del reinicio erróneo y continuar el proceso de restauración**

Después de producirse el error, reinicie el equipo hasta que entre en el entorno de recuperación de Windows (WinRE). Para ello, puede que tenga que usar un conmutador de reinicio de hardware, y es posible que tenga que reiniciar varias veces.

En el entorno de recuperación de Windows:

1. Seleccione **solucionar problemas**  >  **Opciones avanzadas**  >  **más opciones de recuperación**  >  **configuración de inicio** y, después, seleccione **reiniciar ahora**.
1. En la lista de opciones de inicio, seleccione **deshabilitar la aplicación de firmas de controlador**.
   > [!NOTE]  
   > Es posible que tenga que usar la tecla F7 para seleccionar esta opción.
1. Deje que el proceso de inicio continúe. Cuando se reinicia Windows, el proceso de restauración del sistema debe reanudarse y finalizar.

Estos pasos restauran el equipo a su estado "R1".

**Para recuperarse del reinicio erróneo**

Para recuperarse del reinicio erróneo y revertir el proceso de restauración, siga estos pasos:

1. Tal como se describe en el procedimiento anterior, reinicie el equipo y, a continuación, escriba WinRE.  
1. En el entorno de recuperación de Windows, seleccione **solucionar problemas**  >  de **Opciones avanzadas**  >  **Restaurar sistema** y, a continuación, seleccione **Deshacer Restaurar sistema**.

Estos pasos devuelven el equipo al estado en que se encontraba antes de iniciar el proceso de restauración.

**Para restaurar Windows a un punto de restauración mediante WinRE**

Para iniciar el Asistente para restaurar sistema en un equipo afectado, utilice WinRE en lugar del cuadro de diálogo **configuración** . Para ello, siga estos pasos:

1. Seleccione **Inicio**  >  **configuración**  >  **Actualizar & seguridad**  >  **recuperación**.
1. En **Opciones avanzadas**, seleccione **reiniciar ahora**.
1. Cuando se inicie WinRE, seleccione **solucionar problemas** de  >  **Opciones avanzadas**  >  **Restaurar sistema**.
1. Escriba la clave de recuperación tal como se muestra en la pantalla y, a continuación, siga las instrucciones del Asistente para restaurar sistema.

### <a name="references"></a>Referencias

Para obtener más información sobre cómo usar WinRE, consulte los siguientes artículos:

- [Entorno de recuperación de Windows (Windows RE)](/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)
- [Inicio del equipo en modo seguro en Windows 10](https://support.microsoft.com/help/12376) 