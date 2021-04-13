---
description: Para recopilar información de seguimiento de la infraestructura de VSS, puede usar la herramienta VssTrace, la herramienta Logman o la herramienta tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Usar herramientas de seguimiento con VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275426"
---
# <a name="using-tracing-tools-with-vss"></a>Usar herramientas de seguimiento con VSS

Para recopilar información de seguimiento de la infraestructura de VSS, puede usar la herramienta VssTrace, la herramienta Logman o la herramienta tracelog. VssTrace está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows y se puede usar para realizar un seguimiento de las aplicaciones VSS en Windows 7 y versiones posteriores del sistema operativo Windows. Logman es un controlador de seguimiento para los eventos de seguimiento y los contadores de rendimiento. también se puede usar para realizar un seguimiento de las aplicaciones VSS en Windows 7 y versiones posteriores del sistema operativo Windows. Tracelog se incluye en el kit de controladores de Windows (WDK).

Para usar las herramientas de seguimiento con [recuperación automática del sistema (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), consulte [usar herramientas de seguimiento con aplicaciones de ASR](using-tracing-tools-with-vss-asr-applications.md).

> [!Note]  
> VssTrace, Logman y tracelog requieren privilegios de administrador.

 

Para obtener información acerca de cada herramienta, vea las siguientes secciones:

-   [Usar VssTrace](#using-vsstrace)
    -   [Opciones de Command-Line de VssTrace](#vsstrace-command-line-options)
-   [Usar Logman](#using-logman)
-   [Usar tracelog](#using-tracelog)

## <a name="using-vsstrace"></a>Usar VssTrace

Para ejecutar la herramienta VssTrace desde la línea de comandos, use la siguiente sintaxis:

 *Opciones de la línea de comandos de* vsstrace

Para mostrar la ayuda de línea de comandos concisa para la herramienta VssTrace, use la siguiente sintaxis:

**vsstrace-ayuda**

Para mostrar ayuda detallada de la línea de comandos para la herramienta VssTrace, use la siguiente sintaxis:

**vsstrace-help all**

### <a name="vsstrace-command-line-options"></a>Opciones de Command-Line de VssTrace

La herramienta VssTrace utiliza las siguientes opciones de la línea de comandos:

<dl> <dt>

<span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f (** *marcas* )
</dt> <dd>

Habilite los módulos cuyas marcas se especifican en *la máscara de* la máscara. Cada marca corresponde a un módulo de VSS. Si *Flags* es cero, no se habilita ningún módulo. Tenga en cuenta que la mayoría de los módulos están habilitados de forma predeterminada. Esta opción se puede combinar con la **+** opción _Module_ . Por ejemplo, **vsstrace-f 0 + Writer + coords** deshabilita el seguimiento de todos los módulos que están habilitados de forma predeterminada y habilita el seguimiento de escritores de VSS y el servicio VSS. Como alternativa, **vsstrace + f 0xFFFF-coordenadas** permite el seguimiento de todos los módulos excepto el servicio VSS.

> [!Note]  
> Si usa la opción **-f** junto con la **+** opción de _módulo_ , el **-f** debe aparecer antes de la opción de **+** _módulo_ .

 

En la tabla siguiente se enumeran el nombre del módulo y la marca de cada módulo disponible.

| Módulo | Marca       | Habilitado de forma predeterminada | Elementos con seguimiento                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| EXCEPT | 0x00000001 | Sí                | Control de excepciones de C++.                                                                                                                       |
| COORDS  | 0x00000002 | Sí                | El servicio VSS, que también se denomina Coordinador de VSS.                                                                                    |
| SWPRV  | 0x00000004 | Sí                | El servicio de proveedor de instantáneas de sistema de VSS.                                                                                                  |
| BUCOMP | 0x00000008 | Sí                | El solicitante de VSS y el procesamiento de metadatos de copia de seguridad.                                                                                             |
| WRITER | 0x00000010 | Sí                | VSS Writer operaciones y las implementaciones del escritor hospedado de VSS, como el sistema de escritura del registro de Windows.                                             |
| VSSAPI | 0x00000020 | Sí                | Funciones varias de la API de VSS exportadas por VSSAPI.DLL.                                                                                |
| HWDIAG | 0x00000040 | Sí                | Operaciones y infraestructura del proveedor de hardware de VSS.                                                                                          |
| ADMIN  | 0x00000080 | Sí                | Utilidades de línea de comandos de VSS como VSSADMIN.EXE y DISKSHADOW.EXE.                                                                           |
| VSSUI  | 0x00000100 | Sí                | La interfaz de usuario (UI) de configuración de Instantáneas para carpetas compartidas. La interfaz de usuario solo está disponible en los sistemas operativos Windows Server.         |
| PRUEBA   | 0x00000200 | Sí                | No es aplicable. (Este módulo de seguimiento está reservado).                                                                                            |
| INSERCIÓN  | 0x00000400 | Sí                | Detalles de las operaciones de FSCTL y IOCTL que ha iniciado el servicio VSS mediante una llamada a la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) . |
| Group    | 0x00000800 | Sí                | Funciones generales de la utilidad VSS, como asignadores, clases de cadena y operaciones de registro y de volumen.                                        |
| WRXML  | 0x00001000 | No                 | Procesamiento XML para metadatos del escritor. Este módulo tiene un nivel muy alto de ruido.                                                               |
| VSSXML | 0x00002000 | No                 | Clases base de procesamiento XML. Este módulo tiene un nivel muy alto de ruido.                                                                      |



 

</dd> <dt>

<span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Destina_
</dt> <dd>

Habilite el módulo especificado por *módulo*. Se puede habilitar más de un módulo a la vez. Para enumerar los módulos disponibles, escriba **vsstrace – Help modules** en el símbolo de la línea de comandos.

</dd> <dt>

<span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Destina_
</dt> <dd>

Deshabilite el módulo especificado por *módulo*. Para enumerar los módulos disponibles, escriba **vsstrace – Help modules** en el símbolo de la línea de comandos.

</dd> <dt>

<span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+**  ID. de la PID
</dt> <dd>

Habilite el proceso especificado por *ProcessId*. Para habilitar todos los procesos, use " \* " para el valor de *ProcessId*. Se puede especificar más de una opción de **PID** a la vez. El orden de las opciones determina qué procesos están habilitados o deshabilitados. Por ejemplo, para habilitar solo el proceso cuyo identificador de proceso es 0xe8c, use **vsstrace-PID \* + PID 0xe8c**.

</dd> <dt>

<span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-ID. de la PID** 
</dt> <dd>

Deshabilitar el proceso especificado por *ProcessId*. Para deshabilitar todos los procesos, use " \* " para el valor de *ProcessId*. Se puede especificar más de una opción de **PID** a la vez. El orden de las opciones determina qué procesos están habilitados o deshabilitados. Por ejemplo, para deshabilitar todos los procesos excepto el proceso cuyo identificador de proceso es 0xe8c, use **vsstrace-PID \* + PID 0xe8c**.

</dd> <dt>

<span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+** *ThreadId* de TID
</dt> <dd>

Habilita el subproceso especificado por *ThreadId*. Para habilitar todos los subprocesos, use " \* " para el valor de *ThreadId*. Se puede especificar más de una opción de **TID** a la vez. El orden de las opciones determina los subprocesos que están habilitados o deshabilitados. Por ejemplo, para habilitar solo el subproceso cuyo identificador de proceso es 0x31a, use **vsstrace-TID \* + TID 0x31a**.

</dd> <dt>

<span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-ThreadId de TID** 
</dt> <dd>

Deshabilitar el subproceso especificado por *ThreadId*. Para deshabilitar todos los subprocesos, use " \* " para el valor de *ThreadId*. Se puede especificar más de una opción de **TID** a la vez. El orden de las opciones determina los subprocesos que están habilitados o deshabilitados. Por ejemplo, para deshabilitar todos los subprocesos excepto el subproceso cuyo identificador de proceso es 0x31a, use **vsstrace-TID \* + TID 0x31a**.

</dd> <dt>

<span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>*nivel* **-l**
</dt> <dd>

Use el nivel de seguimiento especificado por *nivel*. Cuanto mayor sea el nivel, más detallado será el resultado del seguimiento. Cada nivel incluye todos los niveles inferiores. El nivel predeterminado es 170. Están disponibles los siguientes niveles.



| Nivel | Información incluida en el resultado del seguimiento |
|-------|------------------------------------------|
| 000   | None                                     |
| 020   | Errores graves                             |
| 030   | Excepciones no controladas                     |
| 040   | Errors                                   |
| 050   | Aserciones                               |
| 060   | Advertencias                                 |
| 080   | Control de excepciones                       |
| 100   | Actividad de registro de eventos                       |
| 120   | Información general                      |
| 140   | flujo de código                                |
| 160   | Entrar y salir de la función                  |
| 170   | Valores devueltos de función                   |
| 180   | Parámetros de función (conciso)              |
| 190   | Parámetros de función (detallado)            |
| 200   | Nivel de información detallado 1              |
| 210   | Nivel de información detallado 2              |
| 220   | Nivel de información detallado 3              |
| 230   | Nivel de código rápido 1                        |
| 240   | Nivel de código rápido 2                        |
| 250   | Nivel de código rápido 3                        |
| 255   | All                                      |



 

</dd> <dt>

<span id="_indent"></span><span id="_INDENT"></span>**+ sangría**
</dt> <dd>

Aplique sangría a la salida del seguimiento con formato en cada función y límite de subfunción.

</dd> <dt>

<span id="-indent"></span><span id="-INDENT"></span>**-aplicar sangría**
</dt> <dd>

No aplique sangría a la salida de seguimiento con formato.

</dd> <dt>

<span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-** *EtlFile* ETL
</dt> <dd>

Convierta el archivo de salida Logman especificado por *EtlFile* en un formato de texto legible.

</dd> <dt>

<span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*
</dt> <dd>

Guarde la información de seguimiento en el archivo de salida especificado por *OutputFile*. Para obtener el mejor rendimiento, el archivo de salida debe estar ubicado en un volumen que no sea parte de la instantánea.

</dd> <dt>

<span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-Help** *HelpOption*
</dt> <dd>

Muestra la ayuda de la línea de comandos tal y como se especifica en *HelpOption*. Los valores de *HelpOption* válidos son **módulos**, **niveles** y **todos**. Al especificar **módulos** , se enumeran los módulos. Al especificar **niveles** , se enumeran los niveles disponibles. Si se especifica **All** , se mostrará la ayuda detallada. Si no se usa ninguna opción, se muestra la ayuda concisa.

</dd> </dl>

## <a name="using-logman"></a>Usar Logman

En el procedimiento siguiente se describe cómo usar Logman con la aplicación VSS.

**Para usar Logman con la aplicación VSS**

1.  Use el siguiente comando para iniciar el seguimiento:

    **Logman Start VSS-o** *x: \\ * * * VSS. ETL-ETS-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170**

    > [!Note]  
    > Reemplace "x: \\ " con la ruta de acceso al directorio donde desea que se almacene el archivo de registro de seguimiento.

     

2.  Use el siguiente comando para detener el seguimiento:

    **Logman STOP VSS-ETS**

El archivo de registro de seguimiento es *x: \\* VSS. ETL.

Para obtener más información acerca de la herramienta Logman, consulte [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Usar tracelog

En el procedimiento siguiente se describe cómo usar tracelog.

**Para usar tracelog**

1.  Cree un archivo de texto denominado VSS. CTL que contenga solo el siguiente texto:

    **9138500e-3648-4edb-aa4c-859e9f7b7c38 VSS**

2.  Use el siguiente comando para iniciar el seguimiento:

    **tracelog-Start VSS-f** *x: \\ * * * VSS. ETL-GUID VSS. CTL: flag de nivel 0xFF-0xAA**

    > [!Note]  
    > Reemplace "x: \\ " con la ruta de acceso al directorio donde desea que se almacene el archivo de registro de seguimiento.

     

3.  Use el siguiente comando para detener el seguimiento:

    **tracelog: detener VSS**

El archivo de registro de seguimiento es *x: \\* VSS. ETL.

Para obtener más información acerca de la herramienta tracelog, consulte [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
