---
title: Configuración de WER
description: Configuración personalizar la experiencia de informes de problemas. Todas estas opciones se pueden establecer mediante directiva de grupo. Algunos también se pueden cambiar en el Centro de acciones para Windows 7 y Windows 8. Para Windows 10, use la función de búsqueda de Configuración para buscar Ver configuración avanzada del sistema.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Windows informes de errores Informe de errores de Windows , configuración
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 4586c4f282cbc5c4e2f683c0764eac048f6c05d22a1972cb0ceb84f9699c7925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442234"
---
# <a name="wer-settings"></a>Configuración de WER

Informe de errores de Windows (WER) proporciona muchas opciones para personalizar la experiencia de informes de problemas. Todas estas opciones se pueden establecer mediante directiva de grupo. Algunos también se pueden cambiar en **el Centro de acciones** para Windows 7 y Windows 8. Por Windows 10, use la función de búsqueda de Configuración para buscar **Ver configuración avanzada del sistema**. La configuración de WER se encuentra en una de las siguientes subclaves del Registro:

-   **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Informe de errores de Windows**
-   **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **Informe de errores de Windows**

## <a name="windows-error-reporting-subkey"></a>Informe de errores de Windows subclave

<dl> <dt>

<span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>

0: deshabilite la limitación de omisión de datos. Si la omisión está deshabilitada o no está configurada como una configuración de directiva, WER limita los datos de forma predeterminada. WER no carga más de un archivo CAB para un informe que contiene datos sobre los mismos tipos de eventos.

</dd> <dd>

1 - Habilitar la limitación de omisión de datos. WER no limita los datos. WER carga archivos CAB adicionales que pueden contener datos sobre los mismos tipos de eventos que un informe cargado anteriormente.

</dd> </dl>

Si se debe habilitar la omisión de la limitación de datos del cliente WER

</dd> <dt>

<span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>1 - Solo parámetros (valor predeterminado en Windows 7)</dd> <dd>2 - Todos los datos (valor predeterminado en Windows Vista)</dd> </dl>

Si se deben archivar parámetros solo o todos los datos

</dd> <dt>

<span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consent \\ DefaultConsent**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>1 - Preguntar siempre (valor predeterminado)</dd> <dd>2 - Solo parámetros</dd> <dd>3 - Parámetros y datos seguros</dd> <dd>4 - Todos los datos</dd> </dl>

Opción de consentimiento predeterminada

</dd> <dt>

<span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consent \\ DefaultOverrideBehavior**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0: el consentimiento vertical invalidará el consentimiento predeterminado (valor predeterminado)</dd> <dd>1- El consentimiento predeterminado invalidará el consentimiento específico de la aplicación</dd> </dl>

Si el consentimiento predeterminado invalida el consentimiento vertical

</dd> <dt>

<span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consent \\ \[ VerticalName\]**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>1 - Preguntar siempre (valor predeterminado)</dd> <dd>2 - Solo parámetros</dd> <dd>3 - Parámetros y datos seguros</dd> <dd>4 - Todos los datos</dd> </dl>

Opción de consentimiento para el complemento WER

</dd> <dt>

<span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**
</dt> <dd>

**REG \_ SZ**

Ruta de acceso del directorio

Directorio de destino en el servidor

</dd> <dt>

<span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**
</dt> <dd>

**REG \_ DWORD**

Número de puerto

Número de puerto que se usará con el servidor corporativo

</dd> <dt>

<span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**
</dt> <dd>

**REG \_ SZ**

El nombre del servidor.

Nombre del servidor corporativo

</dd> <dt>

<span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0 - No (valor predeterminado)</dd> <dd>1: Sí</dd> </dl>

Si se va a usar Windows autenticación integrada

</dd> <dt>

<span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0 - No (valor predeterminado)</dd> <dd>1: Sí</dd> </dl>

Si se va a usar SSL

</dd> <dt>

<span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications ExeName (reemplace " ExeName " por un nombre real de un archivo .exe, por \\ \[ \] \[ \] ejemplo, "notepad.exe")**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:

<dl> <dd>0 - Los procesos con un nombre de imagen ejecutable **\[ de ExeName \]** no requieren que el usuario elija **Depurar** o **Continuar** (valor predeterminado)</dd> <dd>1 - Los procesos con un nombre de imagen ejecutable **\[ exeName \]** requieren que el usuario elija **Depurar** o **Continuar.**</dd> </dl> </dd> <dt>

<span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" " es el nombre del \* valor literal)**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:

<dl> <dd>0- Todos los procesos excepto los especificados explícitamente en la configuración **DebugApplications \\ \[ ExeName \]** no requieren que el usuario elija **Depurar** o **Continuar** (valor predeterminado)</dd> <dd>1 - Todos los procesos excepto los especificados explícitamente en la configuración **DebugApplications \\ \[ ExeName \]** requieren que el usuario elija **Depurar** o **Continuar.**</dd> </dl> </dd> <dt>

<span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0 - Habilitado</dd> <dd>1 - Deshabilitado</dd> </dl>

Habilitación o deshabilitación del archivo

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0- Habilitado (valor predeterminado)</dd> <dd>1 - Deshabilitado</dd> </dl>

Habilitación o deshabilitación de WER

</dd> <dt>

<span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0 - Habilitado</dd> <dd>1 - Deshabilitado</dd> </dl>

Habilitación o deshabilitación de la cola de informes

</dd> <dt>

<span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0 : interfaz de usuario (valor predeterminado)</dd> <dd>1 - Sin interfaz de usuario</dd> </dl>

Habilitación o deshabilitación de la interfaz de usuario de WER

</dd> <dt>

<span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0 - Enviar (valor predeterminado)</dd> <dd>1 - No enviar</dd> </dl>

Si se impide el envío de datos de segundo nivel

</dd> <dt>

<span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**Nombre de la aplicación ExcludedApplications \\ \[\]**
</dt> <dd>

**REG \_ SZ**

Uso [ **de WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)

Lista de aplicaciones excluidas

</dd> <dt>

<span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0 - No (valor predeterminado)</dd> <dd>1: Sí</dd> </dl>

Si se deben enviar todos los informes a la cola del usuario

</dd> <dt>

<span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\ DumpFolder o** **LocalDumps Nombre de aplicación \\ \[ \] \\ DumpFolder**
</dt> <dd>

**REG \_ EXPAND \_ SZ**

Ruta de acceso al directorio. El valor predeterminado es %LOCALAPPDATA% \\ CrashDumps. Si no se usa el valor predeterminado, la aplicación debe asegurarse de que la carpeta tiene una ACL suficiente.

**Windows Vista:** No se admiten los valores del Registro en la clave **LocalDumps.** Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).

Ruta de acceso donde se almacenarán los archivos de volcado.

Tenga en cuenta que la configuración por proceso invalidará cualquier configuración global que exista. Para obtener más información, vea [Recopilar User-Mode volcados de memoria](collecting-user-mode-dumps.md).

Esta configuración no se admite en el subárbol del Registro **HKEY \_ CURRENT \_ USER.**

</dd> <dt>

<span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\ DumpCount o** **LocalDumps Nombre de aplicación \\ \[ \] \\ DumpCount**
</dt> <dd>

**REG \_ DWORD**

Número máximo. El valor predeterminado es 10. Cuando se supera el valor máximo, el archivo de volcado más antiguo de la carpeta se reemplazará por el nuevo archivo de volcado.

**Windows Vista:** No se admiten los valores del Registro en la clave **LocalDumps.** Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con SP1.

Número máximo de archivos de volcado de memoria de la carpeta.

Esta configuración no se admite en el subárbol del Registro **HKEY \_ CURRENT \_ USER.**

</dd> <dt>

<span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\ DumpType o** **LocalDumps Nombre de aplicación \\ \[ \] \\ DumpType**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0 - Volcado personalizado</dd> <dd>1 - Minivolquete (valor predeterminado)</dd> <dd>2 - Volcado completo</dd> </dl>

**Windows Vista:** No se admiten los valores del Registro en la clave **LocalDumps.** Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con SP1.

Tipo de volcado.

Esta configuración no se admite en el subárbol del Registro **HKEY \_ CURRENT \_ USER.**

</dd> <dt>

<span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\ CustomDumpFlags** o **LocalDumps Nombre de aplicación \\ \[ \] \\ CustomDumpFlags**
</dt> <dd>

**REG \_ DWORD**

Uno o varios valores de la [**enumeración MINIDUMP \_ TYPE.**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) El valor predeterminado es {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.

**Windows Vista:** No se admiten los valores del Registro en la clave **LocalDumps.** Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con SP1.

Opciones de volcado personalizadas que se usarán. Este valor solo se usa cuando **DumpType** está establecido en 0.

Esta configuración no se admite en el subárbol del Registro **HKEY \_ CURRENT \_ USER.**

</dd> <dt>

<span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**
</dt> <dd>

**REG \_ DWORD**

Valores posibles:<dl> <dd>0: habilitado (valor predeterminado)</dd> <dd>1: deshabilitado</dd> </dl>

Habilitación o deshabilitación del registro

</dd> <dt>

<span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**
</dt> <dd>

**REG \_ DWORD**

Intervalo de valores posibles: 1–5000. El valor predeterminado es 1000.

Tamaño máximo del archivo, en archivos

</dd> <dt>

<span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**
</dt> <dd>

**REG \_ DWORD**

Intervalo de valores posibles: 1–500. El valor predeterminado es 50.

Tamaño máximo de la cola

</dd> <dt>

<span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**
</dt> <dd>

**REG \_ DWORD**

Número de días

Intervalo entre recordatorios al usuario para buscar soluciones, en días

</dd> <dt>

<span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules! \[ pwszOutOfProcessCallbackDll name including path\]**
</dt> <dd>

**REG \_ DWORD**

Se omite el contenido del valor.

El nombre del valor se usa para capturar el valor pwszOutOfProcessCallbackDll.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este valor del Registro.

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a>Informes de kernel en directo de WER Configuración

La configuración de live kernel reports de WER, que se describe a continuación, se encuentra en la siguiente subclave del Registro:

-   **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **CrashControl**

## <a name="fulllivekernelreports-subkey"></a>Subclave FullLiveKernelReports

<dl> <dt>

<span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

Umbral (en horas) de la frecuencia con la que un solo componente puede crear un volcado de memoria activo completo. Este valor debe ser mayor o igual que **SystemThrottleThreshold.** Si se establece en cero (0), se deshabilitará toda la limitación basada en el tiempo. El valor predeterminado es 168 (7 días).

</dd> <dt>

<span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**
</dt> <dd>

**REG \_ DWORD**

Número máximo de volcados de memoria completos que pueden estar en disco en un momento dado. El valor predeterminado es 1. Si establece este valor en cero (0), se deshabilitará la característica de volcado en directo.

</dd> <dt>

<span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**
</dt> <dd>

**REG \_ QWORD**

Valor [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que indica el último tiempo de informe completo para el sistema o un reportType específico. Esto se usa para calcular si se ha cumplido un umbral de directiva.

</dd> <dt>

<span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

Umbral (en horas) de la frecuencia con la que cualquier componente del sistema puede crear un volcado de memoria completo. El valor predeterminado es 120 (5 días).

</dd> </dl>

## <a name="livekernelreports-subkey"></a>Subclave LiveKernelReports

<dl> <dt>

<span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**
</dt> <dd>

**REG \_ SZ**


Ubicación de almacenamiento redirigida de los informes de kernel en directo. La ubicación predeterminada es %systemroot%\LiveKernelReports. Este valor debe ser una ruta de acceso válida. La ruta de acceso debe estar en formato de ruta de acceso NT. Por ejemplo, \? ?\C:\LiveDumpsFolder.  Para obtener más información sobre los formatos de ruta de acceso, vea [Formatos de ruta de acceso de archivo Windows sistemas](/dotnet/standard/io/file-path-formats).

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WER](wer-reference.md)
</dt> </dl>

 

 
