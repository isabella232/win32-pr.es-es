---
title: Puntos de restauración
description: Los puntos de restauración se crean para permitir a los usuarios elegir los estados anteriores del sistema. Cada punto de restauración contiene la información necesaria para restaurar el sistema al estado elegido. Los puntos de restauración se crean antes de que se realicen cambios clave en el sistema.
ms.assetid: 5f68b377-4293-493e-afaf-f4414c2af1fb
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.date: 12/06/2019
manager: dcscontentpm
ms.custom: CSSTroubleshooting
ms.openlocfilehash: 56cc7035f2e5a152ad90205257fb86ddaef8bf565f8459cb5067874280946db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968044"
---
# <a name="restore-points"></a>Puntos de restauración

Los puntos de restauración se crean para permitir que los usuarios seleccionen un estado del sistema anterior. Cada punto de restauración contiene la información necesaria para restaurar el sistema al estado seleccionado. Los puntos de restauración se crean antes de que se realicen cambios clave en el sistema.

Restaurar sistema administra automáticamente el espacio en disco que se asigna para los puntos de restauración. Purga los puntos de restauración más antiguos para dar espacio a otros nuevos. Restaurar sistema asigna espacio en función del tamaño del disco duro y la versión de Windows que ejecuta el equipo, como se muestra en la tabla siguiente.

|Versión de Windows |Tamaño &nbsp; del disco duro |Restaurar sistema espacio |
| --- | --- | --- |
|Windows 7 y versiones posteriores | > 64 GB |Hasta el cinco por ciento del espacio total en disco o un máximo de 10 GB, lo que sea menor |
|  | &le; 64 GB |Hasta el tres por ciento del espacio total en disco |
|Windows Vista |  |Hasta el 15 % del espacio total en disco o un máximo del 30 % del espacio disponible en disco, lo que sea menor |
|Windows XP | >4 GB |Hasta el 12 % del espacio total en disco<br /><br />Para cambiar el límite de almacenamiento máximo en Windows XP, use el **elemento Sistema** en Panel de control. |
|  | \< 4 GB |Hasta 400 MB |

## <a name="event-triggered-restore-points"></a>Puntos de restauración desencadenados por eventos

Restaurar sistema crea automáticamente un punto de restauración antes de que se produzca cualquiera de los siguientes eventos:

- **Instalación de** aplicaciones (solo se aplica a las aplicaciones que usan un Restaurar sistema compatible con la aplicación). Si la instalación de la aplicación provoca problemas del sistema, el usuario puede restaurar el sistema a un estado que precede a la instalación.
- **Windows de actualización automática o actualización automática.** Windows Update (anteriormente conocido como AutoUpdate) descarga e instala automáticamente Windows actualizaciones. Además, proporciona una manera fácil para que los usuarios descarguen e instalen manualmente las actualizaciones. Restaurar sistema crea un punto de restauración antes de instalar una actualización, ya sea de forma automática o manual.
- **Operación de restauración del sistema**. Restaurar sistema crea automáticamente un punto de restauración como copia de seguridad antes de que se inicie cualquier operación de restauración. Por ejemplo, suponga que un usuario restaura accidentalmente Windows a un punto de restauración incorrecto. Para deshacer esa restauración, el usuario puede restaurar Windows a un punto de restauración anterior al primer punto de restauración. Una Windows se ha restaurado a su estado inicial, el usuario puede repetir el proceso, esta vez seleccionando el punto de restauración correcto.

## <a name="scheduled-restore-points"></a>Puntos de restauración programados

Los usuarios pueden configurar Restaurar sistema crear puntos de restauración a intervalos regulares. Los usuarios también pueden crear y nombrar manualmente un punto de restauración en cualquier momento desde la Restaurar sistema usuario. Estos puntos de restauración se guardan y comprimen y están disponibles en la lista de puntos de restauración.

En Windows 7 y versiones posteriores, Restaurar sistema un punto de restauración programado solo si no se ha creado ningún otro punto de restauración en los siete días anteriores. En Windows Vista, Restaurar sistema crea un punto de control cada 24 horas si no se crearon otros puntos de restauración ese día. En Windows XP, Restaurar sistema crea un punto de control cada 24 horas, independientemente de otras operaciones.

## <a name="known-issue-you-cannot-restore-the-system-to-a-restore-point-after-you-install-a-windows-10-update"></a>Problema conocido: no se puede restaurar el sistema a un punto de restauración después de instalar una Windows 10 actualización.

Considere el caso siguiente:

1. Puede instalar Windows 10 en un equipo limpio.
1. Active la protección del sistema y, a continuación, cree un punto de restauración del sistema denominado "R1".
1. Instale una o varias actualizaciones Windows 10 actualizaciones.
1. Una vez que finalice la instalación de las actualizaciones, restaure el sistema al punto de restauración "R1".

En este escenario, el sistema no se restaura al punto de restauración "R1". En su lugar, el equipo experimenta un error de detección (0xc000021a). El equipo se reinicia, pero el sistema no puede volver al Windows escritorio.

### <a name="cause"></a>Causa

Se trata de un problema conocido en Windows 10.

Durante el proceso de restauración del sistema, Windows temporalmente la restauración de los archivos que están en uso. A continuación, guarda la información en el Registro. Cuando se reinicia el equipo, completa la operación por fases.

En esta situación, Windows restaura los archivos de catálogo y hace que los archivos del controlador (.sys) se restaures cuando se reinicie el equipo. Sin embargo, cuando se reinicia el equipo, Windows carga los controladores existentes antes de restaurar las versiones posteriores de los controladores. Dado que las versiones del controlador no coinciden con las versiones de los archivos de catálogo restaurados, el proceso de reinicio se detiene.

### <a name="workaround"></a>Solución alternativa

**Para recuperarse del reinicio con error y continuar con el proceso de restauración**

Una vez que se produzca el error, reinicie el equipo hasta que entre en Windows Recovery Environment (WinRE). Para ello, es posible que tenga que usar un conmutador de reinicio de hardware y que tenga que reiniciar varias veces.

En el entorno Windows Recovery Environment:

1. Seleccione **Solucionar problemas** opciones avanzadas Más opciones de recuperación Configuración de  >    >    >  **inicio** y, a continuación, seleccione Reiniciar **ahora.**
1. En la lista de opciones de inicio, seleccione **Deshabilitar el cumplimiento de la firma del controlador.**
   > [!NOTE]  
   > Es posible que tenga que usar la tecla F7 para seleccionar esta configuración.
1. Deje que el proceso de inicio continúe. Cuando Windows, el proceso de restauración del sistema debe reanudarse y finalizar.

Estos pasos restauran el equipo a su estado "R1".

**Para recuperarse del reinicio con error**

Para recuperarse del reinicio con error y revertir el proceso de restauración, siga estos pasos:

1. Como se describe en el procedimiento anterior, reinicie el equipo y escriba WinRE.  
1. En el entorno Windows recuperación, seleccione Solucionar problemas opciones avanzadas Restauración del sistema y, a continuación, seleccione Deshacer  >    >   **restauración del sistema.**

Estos pasos devuelven el equipo al estado en el que se encontraba antes de iniciar el proceso de restauración.

**Para restaurar Windows a un punto de restauración mediante WinRE**

Para iniciar el asistente Restaurar sistema en un equipo afectado, use WinRE en lugar de Configuración cuadro **de** diálogo. Para ello, realice los pasos siguientes:

1. Seleccione **Start**  >  **Configuración**  >  Update & Security Recovery (Iniciar Configuración la **recuperación de**  >  **seguridad).**
1. En **Opciones avanzadas,** seleccione **Reiniciar ahora.**
1. Una vez que se inicie WinRE, seleccione **Solucionar**  >  **problemas opciones avanzadas**  >  **Restauración del sistema.**
1. Escriba la clave de recuperación tal como se muestra en la pantalla y, a continuación, siga las instrucciones del asistente Restaurar sistema recuperación.

### <a name="references"></a>Referencias

Para más información sobre cómo usar WinRE, consulte los siguientes artículos:

- [Entorno de recuperación de Windows (Windows RE)](/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)
- [Inicie el equipo en modo seguro en Windows 10](https://support.microsoft.com/help/12376) 