---
description: Para recopilar información de seguimiento para la infraestructura de VSS, puede usar la herramienta VssTrace, la herramienta Logman o la herramienta Tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Uso de herramientas de seguimiento con VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34b79fa91bad210b20d14c2655368f4a5494efe4b462a7a0b93ea672b049d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937747"
---
# <a name="using-tracing-tools-with-vss"></a>Uso de herramientas de seguimiento con VSS

Para recopilar información de seguimiento para la infraestructura de VSS, puede usar la herramienta VssTrace, la herramienta Logman o la herramienta Tracelog. VssTrace está disponible en el Kit de desarrollo de software (SDK) de Microsoft Windows y se puede usar para realizar el seguimiento de aplicaciones VSS en Windows 7 y versiones posteriores del sistema operativo Windows. Logman es un controlador de seguimiento para eventos de seguimiento y contadores de rendimiento. también se puede usar para realizar un seguimiento de las aplicaciones VSS en Windows 7 y versiones posteriores del Windows operativo. Tracelog se incluye en Windows Driver Kit (WDK).

Para usar herramientas de seguimiento [con automated Recuperación del sistema (ASR),](using-vss-automated-system-recovery-for-disaster-recovery.md)vea [Using Tracing Tools with ASR Applications](using-tracing-tools-with-vss-asr-applications.md).

> [!Note]  
> VssTrace, Logman y Tracelog requieren privilegios de administrador.

 

Para obtener información sobre cada herramienta, consulte las secciones siguientes:

-   [Uso de VssTrace](#using-vsstrace)
    -   [Opciones de Command-Line VssTrace](#vsstrace-command-line-options)
-   [Uso de Logman](#using-logman)
-   [Uso de Tracelog](#using-tracelog)

## <a name="using-vsstrace"></a>Uso de VssTrace

Para ejecutar la herramienta VssTrace desde la línea de comandos, use la sintaxis siguiente:

**vsstrace** *command-line-options*

Para mostrar la ayuda concisa de la línea de comandos para la herramienta VssTrace, use la sintaxis siguiente:

**vsstrace -help**

Para mostrar ayuda detallada de la línea de comandos para la herramienta VssTrace, use la sintaxis siguiente:

**vsstrace -help all**

### <a name="vsstrace-command-line-options"></a>Opciones de Command-Line VssTrace

La herramienta VssTrace usa las siguientes opciones de línea de comandos:

<dl> <dt>

<span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *Marcas*
</dt> <dd>

Habilite los módulos cuyas marcas se especifican mediante la máscara de bits *Flags.* Cada marca corresponde a un módulo de VSS. Si *Flags es* cero, no se habilita ningún módulo. Tenga en cuenta que la mayoría de los módulos están habilitados de forma predeterminada. Esta opción se puede combinar con la **+** _opción Module._ Por ejemplo, **vsstrace -f 0 +WRITER +COORD** deshabilita el seguimiento de todos los módulos que están habilitados de forma predeterminada y habilita el seguimiento de escritores de VSS y el servicio VSS. Como alternativa, **vsstrace +f 0xffff -COORD habilita** el seguimiento de todos los módulos excepto el servicio VSS.

> [!Note]  
> Si usa la **opción -f** junto con la **+** _opción Module,_ **-f** debe aparecer antes de la **+** _opción Module._

 

En la tabla siguiente se enumeran el nombre del módulo y la marca de cada módulo disponible.

| Módulo | Marca       | Habilitado de forma predeterminada | Elementos de los que se ha seguimiento                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| EXCEPT | 0x00000001 | Sí                | Control de excepciones de C++.                                                                                                                       |
| Coord  | 0x00000002 | Sí                | El servicio VSS, que también se denomina coordinador de VSS.                                                                                    |
| SWPRV  | 0x00000004 | Sí                | El servicio proveedor de instantáneas del sistema de VSS.                                                                                                  |
| BUCOMP | 0x00000008 | Sí                | El solicitante de VSS y el procesamiento de metadatos de copia de seguridad.                                                                                             |
| WRITER | 0x00000010 | Sí                | Las operaciones de VSS Writer y las implementaciones de vss hosted writer, como Windows escritor del Registro.                                             |
| VSSAPI | 0x00000020 | Sí                | Funciones varias de la API de VSS exportadas por VSSAPI.DLL.                                                                                |
| HWDIAG | 0x00000040 | Sí                | Infraestructura y operaciones del proveedor de hardware de VSS.                                                                                          |
| ADMIN  | 0x00000080 | Sí                | Utilidades de línea de comandos de VSS como VSSADMIN.EXE y DISKSHADOW.EXE.                                                                           |
| VSSUI  | 0x00000100 | Sí                | Interfaz de Instantáneas para carpetas compartidas de usuario (UI) de configuración de datos. La interfaz de usuario solo está disponible en Windows operativos server.         |
| PRUEBA   | 0x00000200 | Sí                | No es aplicable. (Este módulo de seguimiento está reservado).                                                                                            |
| Ioctl  | 0x00000400 | Sí                | Detalles de las operaciones FSCTL e IOCTL que el servicio VSS ha iniciado mediante una llamada a la [**función DeviceIoControl.**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) |
| GEN    | 0x00000800 | Sí                | Funciones generales de la utilidad de VSS, como asignadores, clases de cadena y operaciones de registro y volumen.                                        |
| WRXML  | 0x00001000 | No                 | Procesamiento XML para metadatos de escritor. Este módulo tiene un nivel muy alto de ruido.                                                               |
| VSSXML | 0x00002000 | No                 | Clases base de procesamiento XML. Este módulo tiene un nivel muy alto de ruido.                                                                      |



 

</dd> <dt>

<span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Módulo_
</dt> <dd>

Habilite el módulo especificado por *Module*. Se puede habilitar más de un módulo a la vez. Para enumerar los módulos disponibles, escriba **vsstrace –help modules** en el símbolo de la línea de comandos.

</dd> <dt>

<span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Módulo_
</dt> <dd>

Deshabilite el módulo especificado por *Module*. Para enumerar los módulos disponibles, escriba **vsstrace –help modules** en el símbolo de la línea de comandos.

</dd> <dt>

<span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+pid** *ProcessId*
</dt> <dd>

Habilite el proceso especificado por *ProcessId.* Para habilitar todos los procesos, use " \* " como valor de *ProcessId*. Se puede **especificar más de** una opción pid a la vez. El orden de las opciones determina qué procesos están habilitados o deshabilitados. Por ejemplo, para habilitar solo el proceso cuyo identificador de proceso 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.

</dd> <dt>

<span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*
</dt> <dd>

Deshabilite el proceso especificado por *ProcessId.* Para deshabilitar todos los procesos, use " \* " como valor de *ProcessId*. Se puede **especificar más de** una opción pid a la vez. El orden de las opciones determina qué procesos están habilitados o deshabilitados. Por ejemplo, para deshabilitar todos los procesos excepto el proceso cuyo identificador de proceso 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.

</dd> <dt>

<span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+tid** *ThreadId*
</dt> <dd>

Habilite el subproceso especificado por *ThreadId.* Para habilitar todos los subprocesos, use " \* " para el valor de *ThreadId*. Se puede **especificar más de** una opción de tipo a la vez. El orden de las opciones determina qué subprocesos están habilitados o deshabilitados. Por ejemplo, para habilitar solo el subproceso cuyo identificador de proceso 0x31a, use **vsstrace -tid \* +tid 0x31a**.

</dd> <dt>

<span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*
</dt> <dd>

Deshabilite el subproceso especificado por *ThreadId.* Para deshabilitar todos los subprocesos, use " \* " para el valor de *ThreadId*. Se puede **especificar más de** una opción de tipo a la vez. El orden de las opciones determina qué subprocesos están habilitados o deshabilitados. Por ejemplo, para deshabilitar todos los subprocesos excepto el subproceso cuyo identificador de proceso 0x31a, use **vsstrace -tid \* +tid 0x31a**.

</dd> <dt>

<span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *Nivel*
</dt> <dd>

Use el nivel de seguimiento especificado por *Level*. Cuanto mayor sea el nivel, más detallada será la salida de seguimiento. Cada nivel incluye todos los niveles inferiores. El nivel predeterminado es 170. Los niveles siguientes están disponibles.



| Nivel | Información incluida en la salida de seguimiento |
|-------|------------------------------------------|
| 000   | Ninguno                                     |
| 020   | Errores graves                             |
| 030   | Excepciones no controladas                     |
| 040   | Errors                                   |
| 050   | Aserciones                               |
| 060   | Advertencias                                 |
| 080   | Control de excepciones                       |
| 100   | Actividad del registro de eventos                       |
| 120   | Información general                      |
| 140   | flujo de código                                |
| 160   | Entrada y salida de la función                  |
| 170   | Valores devueltos de la función                   |
| 180   | Parámetros de función (dispersos)              |
| 190   | Parámetros de función (detallado)            |
| 200   | Nivel de información detallada 1              |
| 210   | Nivel de información detallada 2              |
| 220   | Nivel de información detallada 3              |
| 230   | Nivel de código rápido 1                        |
| 240   | Nivel de código rápido 2                        |
| 250   | Nivel de código rápido 3                        |
| 255   | Todo                                      |



 

</dd> <dt>

<span id="_indent"></span><span id="_INDENT"></span>**+sangría**
</dt> <dd>

Aplicar sangría a la salida de seguimiento con formato en cada función y límite de subfunción.

</dd> <dt>

<span id="-indent"></span><span id="-INDENT"></span>**-indent**
</dt> <dd>

No aplique sangría a la salida de seguimiento con formato.

</dd> <dt>

<span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*
</dt> <dd>

Convierta el archivo de salida de Logman especificado por *EtlFile* en un formato de texto legible.

</dd> <dt>

<span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*
</dt> <dd>

Guarde la información de seguimiento en el archivo de salida especificado por *OutputFile*. Para obtener el mejor rendimiento, el archivo de salida debe estar ubicado en un volumen que no forma parte de la instantánea.

</dd> <dt>

<span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*
</dt> <dd>

Muestre la ayuda de la línea de comandos especificada por *HelpOption.* Los valores *válidos de HelpOption* **son módulos**, **niveles** y **todos**. Si se **especifican módulos,** se mostrarán los módulos. Si se **especifican niveles,** se mostrarán los niveles disponibles. Si se **especifica todo,** se mostrará ayuda detallada. Si no se usa ninguna opción, se muestra ayuda concisa.

</dd> </dl>

## <a name="using-logman"></a>Uso de Logman

En el procedimiento siguiente se describe cómo usar Logman con la aplicación VSS.

**Para usar Logman con la aplicación VSS**

1.  Use el siguiente comando para iniciar el seguimiento:

    **logman start vss -o** *x: \\ {vss.etl -ets -p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170**

    > [!Note]  
    > Reemplace "x: " por la ruta de acceso al directorio donde desea almacenar el archivo de \\ registro de seguimiento.

     

2.  Use el siguiente comando para detener el seguimiento:

    **logman stop vss -ets**

El archivo de registro de seguimiento *es x: \\* vss.etl.

Para obtener más información sobre la herramienta Logman, vea [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Uso de Tracelog

En el procedimiento siguiente se describe cómo usar Tracelog.

**Para usar Tracelog**

1.  Cree un archivo de texto denominado vss.ctl que contenga solo el texto siguiente:

    **9138500e-3648-4edb-aa4c-859e9f7b7c38 vss**

2.  Use el siguiente comando para iniciar el seguimiento:

    **tracelog -start vss -f** *x: \\ %(vss.etl -guid vss.ctl -flag 0xff -level 0xaa**

    > [!Note]  
    > Reemplace "x: " por la ruta de acceso al directorio donde desea almacenar el archivo de \\ registro de seguimiento.

     

3.  Use el siguiente comando para detener el seguimiento:

    **tracelog -stop vss**

El archivo de registro de seguimiento *es x: \\* vss.etl.

Para obtener más información sobre la herramienta Tracelog, vea [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
