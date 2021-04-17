---
title: Configuración de WER
description: Configuración para personalizar la experiencia de informes de problemas. Todos estos valores se pueden establecer mediante directiva de grupo. Algunos también se pueden cambiar en el centro de actividades para Windows 7 y Windows 8. En el caso de Windows 10, use la función de búsqueda en configuración para ver la configuración avanzada del sistema.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Informe de errores de Windows Informe de errores de Windows, configuración
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "105653267"
---
# <a name="wer-settings"></a>Configuración de WER

Informe de errores de Windows (WER) proporciona muchas opciones para personalizar la experiencia de informes de problemas. Todos estos valores se pueden establecer mediante directiva de grupo. Algunos también se pueden cambiar en el **centro de actividades** para Windows 7 y Windows 8. En el caso de Windows 10, use la función de búsqueda en configuración para **ver la configuración avanzada del sistema**. La configuración de WER se encuentra en una de las siguientes subclaves del registro:

-   **HKEY \_ Software de \_ usuario actual** \\  \\ **Microsoft** \\ **Windows** \\ **Informe de errores de Windows**
-   **HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **Informe de errores de Windows**

## <a name="windows-error-reporting-subkey"></a>Subclave Informe de errores de Windows

<dl> <dt>

<span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>

0: deshabilitar la limitación de derivación de datos. Si la omisión está deshabilitada o no está configurada como una configuración de Directiva, WER limita los datos de forma predeterminada. WER no carga más de un archivo CAB para un informe que contiene datos sobre los mismos tipos de eventos.

</dd> <dd>

1-habilitar la limitación de derivación de datos. WER no limita los datos. WER carga archivos CAB adicionales que pueden contener datos sobre los mismos tipos de eventos que un informe cargado anteriormente.

</dd> </dl>

Indica si se debe habilitar la omisión de la limitación de datos del cliente de WER

</dd> <dt>

<span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>1-solo parámetros (valor predeterminado en Windows 7)</dd> <dd>2-todos los datos (predeterminado en Windows Vista)</dd> </dl>

Si se van a archivar solo los parámetros o todos los datos

</dd> <dt>

<span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**DefaultConsent de consentimiento \\**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>1-preguntar siempre (valor predeterminado)</dd> <dd>2-solo parámetros</dd> <dd>3-parámetros y datos seguros</dd> <dd>4-todos los datos</dd> </dl>

Elección de consentimiento predeterminado

</dd> <dt>

<span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**DefaultOverrideBehavior de consentimiento \\**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0: el consentimiento vertical invalidará el consentimiento predeterminado (valor predeterminado)</dd> <dd>1: el consentimiento predeterminado invalidará el consentimiento específico de la aplicación.</dd> </dl>

Si el consentimiento predeterminado invalida el consentimiento vertical

</dd> <dt>

<span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**VerticalName de consentimiento \\ \[\]**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>1-preguntar siempre (valor predeterminado)</dd> <dd>2-solo parámetros</dd> <dd>3-parámetros y datos seguros</dd> <dd>4-todos los datos</dd> </dl>

Elección de consentimiento para el complemento WER

</dd> <dt>

<span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**
</dt> <dd>

**Registro \_ SZ**

La ruta de acceso del directorio

Directorio de destino en el servidor

</dd> <dt>

<span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**
</dt> <dd>

**\_valor DWORD reg**

El número de Puerto

Número de puerto que se va a usar con el servidor corporativo

</dd> <dt>

<span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**
</dt> <dd>

**Registro \_ SZ**

El nombre del servidor.

Nombre del servidor corporativo

</dd> <dt>

<span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0: no (valor predeterminado)</dd> <dd>1: Sí</dd> </dl>

Si se va a usar la autenticación integrada de Windows

</dd> <dt>

<span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0: no (valor predeterminado)</dd> <dd>1: Sí</dd> </dl>

Si se va a usar SSL

</dd> <dt>

<span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ ExeName \] (reemplace " \[ ExeName \] " por el nombre real de un archivo. exe, por ejemplo, "notepad.exe")**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:

<dl> <dd>0: los procesos con el nombre de la imagen ejecutable de **\[ ExeName \]** no requieren que el usuario elija **depurar** o **continuar** (valor predeterminado)</dd> <dd>1: los procesos con el nombre de la imagen ejecutable de **\[ ExeName \]** requieren que el usuario elija **depurar** o **continuar** .</dd> </dl> </dd> <dt>

<span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" \* " es el nombre del valor literal)**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:

<dl> <dd>0: todos los procesos excepto los especificados explícitamente en el valor **DebugApplications \\ \[ ExeName \]** no requieren que el usuario elija **depurar** o **continuar** (valor predeterminado).</dd> <dd>1-todos los procesos excepto los especificados explícitamente en el valor de **DebugApplications \\ \[ ExeName \]** requieren que el usuario elija **depurar** o **continuar** .</dd> </dl> </dd> <dt>

<span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0 - Habilitado</dd> <dd>1 - Deshabilitado</dd> </dl>

Habilitar o deshabilitar el archivo

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disponible**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0: habilitado (valor predeterminado)</dd> <dd>1 - Deshabilitado</dd> </dl>

Habilitar o deshabilitar WER

</dd> <dt>

<span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0 - Habilitado</dd> <dd>1 - Deshabilitado</dd> </dl>

Habilitar o deshabilitar la puesta en cola de informes

</dd> <dt>

<span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0: interfaz de usuario (valor predeterminado)</dd> <dd>1-sin interfaz de usuario</dd> </dl>

Habilitar o deshabilitar la interfaz de usuario de WER

</dd> <dt>

<span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0: enviar (valor predeterminado)</dd> <dd>1: no enviar</dd> </dl>

Si se va a impedir el envío de datos de segundo nivel

</dd> <dt>

<span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**Nombre de la \\ \[ aplicación ExcludedApplications\]**
</dt> <dd>

**Registro \_ SZ**

Usar [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)

Lista de aplicaciones excluidas

</dd> <dt>

<span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0: no (valor predeterminado)</dd> <dd>1: Sí</dd> </dl>

Si se van a enviar todos los informes a la cola del usuario

</dd> <dt>

<span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\ DumpFolder** o **LocalDumps \\ \[ nombre de aplicación \] \\ DumpFolder**
</dt> <dd>

**REG \_ expandir \_ SZ**

Ruta de acceso al directorio. El valor predeterminado es% LOCALAPPDATA% \\ CrashDumps. Si no se usa el valor predeterminado, la aplicación debe asegurarse de que la carpeta tiene una ACL suficiente.

**Windows Vista:** No se admiten los valores del registro en la clave **LocalDumps** . Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

La ruta de acceso donde se almacenarán los archivos de volcado.

Tenga en cuenta que la configuración por proceso invalidará cualquier configuración global que exista para obtener más información, consulte [recopilación de volcados de User-Mode](collecting-user-mode-dumps.md).

Esta configuración no se admite en el subárbol del registro de **\_ \_ usuario actual HKEY** .

</dd> <dt>

<span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\ DumpCount** o **LocalDumps \\ \[ nombre de aplicación \] \\ DumpCount**
</dt> <dd>

**\_valor DWORD reg**

Número máximo. El valor predeterminado es 10. Cuando se supera el valor máximo, el archivo de volcado más antiguo de la carpeta se reemplazará por el nuevo archivo de volcado de memoria.

**Windows Vista:** No se admiten los valores del registro en la clave **LocalDumps** . Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con SP1.

Número máximo de archivos de volcado en la carpeta.

Esta configuración no se admite en el subárbol del registro de **\_ \_ usuario actual HKEY** .

</dd> <dt>

<span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\ DumpType** o **LocalDumps \\ \[ nombre de aplicación \] \\ DumpType**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0: volcado de memoria personalizado</dd> <dd>1-minivolcado (predeterminado)</dd> <dd>2-volcado completo</dd> </dl>

**Windows Vista:** No se admiten los valores del registro en la clave **LocalDumps** . Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con SP1.

El tipo de volcado.

Esta configuración no se admite en el subárbol del registro de **\_ \_ usuario actual HKEY** .

</dd> <dt>

<span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\ CustomDumpFlags** o **LocalDumps \\ \[ nombre de aplicación \] \\ CustomDumpFlags**
</dt> <dd>

**\_valor DWORD reg**

Uno o más valores de la enumeración de [**\_ tipo de minivolcado**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) . El valor predeterminado es {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.

**Windows Vista:** No se admiten los valores del registro en la clave **LocalDumps** . Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con SP1.

Opciones de volcado de memoria personalizadas que se van a utilizar. Este valor solo se usa cuando **DumpType** se establece en 0.

Esta configuración no se admite en el subárbol del registro de **\_ \_ usuario actual HKEY** .

</dd> <dt>

<span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**
</dt> <dd>

**\_valor DWORD reg**

Valores posibles:<dl> <dd>0: habilitado (valor predeterminado)</dd> <dd>1: deshabilitado</dd> </dl>

Habilitar o deshabilitar el registro

</dd> <dt>

<span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**
</dt> <dd>

**\_valor DWORD reg**

Rango de valores posibles: 1 – 5000. El valor predeterminado es 1000.

Tamaño máximo del archivo, en archivos

</dd> <dt>

<span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**
</dt> <dd>

**\_valor DWORD reg**

Rango de valores posibles: 1 – 500. El valor predeterminado es 50.

Tamaño máximo de la cola

</dd> <dt>

<span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**
</dt> <dd>

**\_valor DWORD reg**

Número de días

Intervalo entre recordatorios al usuario para buscar soluciones, en días

</dd> <dt>

<span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules! \[ nombre de pwszOutOfProcessCallbackDll que incluye la ruta de acceso\]**
</dt> <dd>

**\_valor DWORD reg**

Se omite el contenido del valor.

El nombre del valor se usa para capturar el valor de pwszOutOfProcessCallbackDll.

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite este valor del registro.

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a>Configuración de informes de kernel Live de WER

La configuración de informes de kernel en directo de WER, que se describe a continuación, se encuentra en la siguiente subclave del registro:

-   **HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local CrashControl

## <a name="fulllivekernelreports-subkey"></a>Subclave FullLiveKernelReports

<dl> <dt>

<span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**
</dt> <dd>

**\_valor DWORD reg**

El umbral (en horas) de la frecuencia con la que cualquier componente individual puede crear un volcado en vivo completo. Este valor debe ser mayor o igual que **SystemThrottleThreshold**. Si se establece en cero (0), se deshabilitará toda la limitación basada en el tiempo. El valor predeterminado es 168 (7 días).

</dd> <dt>

<span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**
</dt> <dd>

**\_valor DWORD reg**

El número máximo de volcados en vivo completos que pueden estar en el disco en un momento dado. El valor predeterminado es 1. Si se establece este valor en cero (0), se deshabilitará la característica de volcado en vivo.

</dd> <dt>

<span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**
</dt> <dd>

**QWord de REG \_**

Un [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que indica la hora del último informe activo, del sistema o de un reportType específico. Se usa para calcular si se ha satisfecho un umbral de la Directiva.

</dd> <dt>

<span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**
</dt> <dd>

**\_valor DWORD reg**

El umbral (en horas) de la frecuencia con la que cualquier componente del sistema puede crear un volcado en vivo completo. El valor predeterminado es 120 (5 días).

</dd> </dl>

## <a name="livekernelreports-subkey"></a>Subclave LiveKernelReports

<dl> <dt>

<span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**
</dt> <dd>

**Registro \_ SZ**


La ubicación de almacenamiento Redirigido de los informes de kernel en vivo. La ubicación predeterminada es%systemroot%\LiveKernelReports. Este valor debe ser una ruta de acceso válida. La ruta de acceso debe tener el formato de ruta de acceso NT. Por ejemplo, \? ? \c: \LiveDumpsFolder.  Para obtener más información sobre los formatos de ruta de acceso, vea  [formatos de ruta de acceso de archivo en sistemas Windows](/dotnet/standard/io/file-path-formats).

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WER](wer-reference.md)
</dt> </dl>

 

 
