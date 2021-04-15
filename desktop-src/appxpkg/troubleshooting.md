---
title: Solución de problemas de empaquetado, implementación y consulta de aplicaciones de Windows
description: Siga estas sugerencias para solucionar los problemas que experimente al empaquetar, implementar o consultar un paquete de la aplicación.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/25/2021
ms.locfileid: "105709280"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>Solución de problemas de empaquetado, implementación y consulta de aplicaciones de Windows

Siga estas sugerencias para solucionar los problemas que experimente al empaquetar, implementar o consultar un paquete de aplicación de Windows (. msix/. appx) como desarrollador.

> [!NOTE]
> Este artículo está destinado a los desarrolladores. Si no es un desarrollador y busca ayuda con un error de instalación de aplicación de Windows, consulte [soporte técnico de Windows](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).

## <a name="get-diagnostic-information"></a>Obtención de información de diagnóstico

Cuando se produce un error en una API, devuelve un código de error que describe el problema. Si el código de error no proporciona suficiente información, encontrará más información de diagnóstico en los registros de eventos detallados.

Para obtener acceso a los registros de eventos de empaquetado e implementación mediante **visor de eventos**, siga estos pasos:

1. Realice uno de estos pasos:

    * Haga clic en **Inicio** en el menú Windows, escriba **visor de eventos** y **presione Entrar**.
    * Ejecute **eventvwr. msc**.

2. En la página de la izquierda, expanda **visor de eventos (local)**  >  **registros de aplicaciones y servicios**  >  **Microsoft**  >  **Windows**.
3. Compruebe si hay registros disponibles en estas categorías:

    * **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**
    * **AppXDeployment: servidor**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**

Para empezar, consulte los registros en **AppXDeployment-Server**. Si el error se debe a **0x80073CF0** o **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, pueden aparecer detalles adicionales en los registros de **AppxpackagingOM** .

También puede usar el comando [Get-AppxLog](/powershell/module/appx/get-appxlog) en PowerShell para obtener los primeros eventos registrados. En el ejemplo siguiente se muestran los registros asociados con la operación de implementación más reciente.

```PowerShell
Get-Appxlog
```

En el ejemplo siguiente se muestran los registros asociados con la operación de implementación más reciente en una tabla interactiva en una ventana independiente.

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>Códigos comunes de error

En esta tabla se enumeran algunos de los códigos de error más comunes. Si necesita más ayuda con uno de estos errores, o si encuentra un código de error que no está en esta lista, consulte Opciones de [ayuda adicionales](#get-additional-help).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Código de error</th>
<th>Value</th>
<th>Descripción y causas posibles</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><strong>E_FILENOTFOUND</strong></td>
<td>0x80070002</td>
<td>El archivo o la ruta de acceso no se encuentra. Esto puede ocurrir durante la validación de la biblioteca de bibliotecas COM requiere que la ruta de acceso del directorio exista realmente en el paquete MSIX.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_BAD_FORMAT</strong></td>
<td>0x8007000B</td>
<td>El paquete no tiene el formato correcto y debe volver a generarse o firmarse.<br/> Este error puede aparecer si hay una discrepancia entre el nombre de sujeto del certificado de firma y el nombre del publicador de AppxManifest.xml.<br/> Consulte <a href="how-to-sign-a-package-using-signtool.md">cómo firmar un paquete de aplicación mediante SignTool</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>E_INVALIDARG</strong></td>
<td>0x80070057</td>
<td>Uno o varios argumentos no son válidos. Si comprueba la AppXDeployment-Server registro de eventos y ve el siguiente evento: "al instalar el paquete, el sistema no pudo registrar la extensión Windows. repositoryExtension debido al siguiente error: el parámetro es incorrecto". <br/> Este error puede aparecer si el elemento de manifiesto DisplayName o Description contiene caracteres no permitidos por Firewall de Windows; es decir, |  y todo, debido a que Windows no puede crear el perfil de AppContainer para el paquete. Quite estos caracteres del manifiesto e intente instalar el paquete. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPEN_</strong><br/> <strong>PACKAGE_FAILED</strong><br/></td>
<td>0x80073CF0</td>
<td>No se pudo abrir el paquete.<br/> Causas posibles:<br/>
<ul>
<li>El paquete no está firmado.</li>
<li>El nombre del publicador no coincide con el firmante del certificado de firma.</li>
<li>Falta el prefijo file://o el paquete no se pudo encontrar en la ubicación especificada.</li>
</ul>
Para obtener más información, consulte el registro de eventos <strong>AppxPackagingOM</strong> .<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_PACKAGE_</strong><br/> <strong>NOT_FOUND</strong><br/></td>
<td>0x80073CF1</td>
<td>No se pudo encontrar el paquete.<br/> Puede obtener este error al quitar un paquete que no está instalado para el usuario actual.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>CONFIGURA</strong><br/></td>
<td>0x80073CF2</td>
<td>Los datos del paquete no son válidos.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_RESOLVE_</strong><br/> <strong>DEPENDENCY_FAILED</strong><br/></td>
<td>0x80073CF3</td>
<td>Error de actualización, dependencia o validación de conflicto en el paquete.<br/> Causas posibles:<br/>
<ul>
<li>El paquete entrante entra en conflicto con un paquete instalado.</li>
<li>No se encuentra una dependencia del paquete especificada.</li>
<li>El paquete no es compatible con la arquitectura de procesador correcta.</li>
</ul>
Para obtener más informtion, consulte el registro de eventos <strong>de AppXDeployment-Server</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OUT_</strong><br/> <strong>OF_DISK_SPACE</strong><br/></td>
<td>0x80073CF4</td>
<td>No hay suficiente espacio en disco en el equipo. Libere espacio y vuelva a intentarlo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_NETWORK_</strong><br/> <strong>FALLIDA</strong><br/></td>
<td>0x80073CF5</td>
<td>No se puede descargar el paquete.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>REGISTRATION_FAILURE</strong><br/></td>
<td>0x80073CF6</td>
<td>No se puede registrar el paquete.<br/> Para obtener más información, consulte el registro de eventos de <strong>AppXDeployment-Server</strong> .<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>DEREGISTRATION_EFAILURE</strong><br/></td>
<td>0x80073CF7</td>
<td>No se puede anular el registro del paquete.<br/> Puede obtener este error al quitar un paquete.<br/> Para obtener más información, consulte el registro de eventos de <strong>AppXDeployment-Server</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_CANCEL</strong></td>
<td>0x80073CF8</td>
<td>El usuario canceló la solicitud de instalación.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_FAILED</strong></td>
<td>0x80073CF9</td>
<td>No se pudo instalar el paquete. Póngase en contacto con el proveedor de software.<br/> Para obtener más información, consulte el registro de eventos de <strong>AppXDeployment-Server</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_REMOVE_FAILED</strong></td>
<td>0x80073CFA</td>
<td>No se pudo quitar el paquete.<br/> Puede obtener este error en caso de errores que se produzcan durante la desinstalación del paquete.<br/> Para obtener más información, vea <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>ALREADY_EXISTS</strong><br/></td>
<td>0x80073CFB</td>
<td>El paquete suministrado ya está instalado y se ha bloqueado la reinstalación del paquete. <br/> Puede obtener este error si instala un paquete que no es idéntico bit a bit al paquete que ya está instalado. Tenga en cuenta que la firma digital también forma parte del paquete. Por lo tanto, si se vuelve a generar o se vuelve a firmar un paquete, ya no es idéntico bit a bit al paquete instalado previamente. Dos opciones posibles para corregir este error son: (1) incrementar el número de versión de la aplicación y, a continuación, volver a generar y firmar el paquete (2) quitar el paquete antiguo para todos los usuarios del sistema antes de instalar el nuevo paquete. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REMEDIATION</strong></td>
<td>0x80073CFC</td>
<td>No se puede iniciar la aplicación. Intente volver a instalar la aplicación.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PREREQUISITE_FAILED</strong><br/></td>
<td>0x80073CFD</td>
<td>No se pudo satisfacer un requisito previo de instalación especificado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>REPOSITORY_CORRUPTED</strong><br/></td>
<td>0x80073CFE</td>
<td>El repositorio de paquetes está dañado.<br/> Puede obtener este error si la carpeta a la que hace referencia esta clave del registro no existe o está dañada: <br/> <strong>HKLM\SOFTWARE\Microsoft\Windows</strong><br/> <strong>CurrentVersion\Appx\PackageRepositoryRoot</strong><br/> Para recuperarse de este estado, actualice el equipo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>POLICY_FAILURE</strong><br/></td>
<td>0x80073CFF</td>
<td>Para instalar esta aplicación, necesita una licencia de desarrollador o un sistema habilitado para instalación de prueba. <br/> Es posible que reciba este error si el paquete no cumple uno de los siguientes requisitos:<br/>
<ul>
<li>La aplicación se implementa con F5 en Visual Studio en un equipo con una licencia de desarrollador de Windows.</li>
<li>El paquete se firma con una firma de Microsoft y se implementa como parte de Windows o desde el Microsoft Store.</li>
<li>El paquete se firma con una firma de confianza y se instala en un equipo con una licencia de desarrollador, un equipo unido a un dominio con la Directiva AllowAllTrustedApps habilitada, o un equipo con una licencia de instalación de prueba de Windows con la Directiva AllowAllTrustedApps habilitada.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_UPDATING</strong></td>
<td>0x80073D00</td>
<td>No se puede iniciar la aplicación porque se está actualizando.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_</strong><br/> <strong>BLOCKED_BY_POLICY</strong><br/></td>
<td>0x80073D01</td>
<td>La Directiva bloquea la operación de implementación de paquetes. Póngase en contacto con el administrador del sistema.<br/> Causas posibles:<br/>
<ul>
<li>Las directivas de control de aplicaciones bloquean la implementación de paquetes.</li>
<li>La implementación de paquetes está bloqueada por la &quot; Directiva permitir operaciones de implementación en perfiles especiales &quot; .</li>
</ul>
Uno de los motivos posibles es una necesidad de un perfil móvil. Para obtener información acerca de cómo configurar perfiles de usuario móviles en cuentas de usuario, consulte <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">implementar perfiles de usuario móviles</a>. Si no hay directivas configuradas en el sistema y sigue viendo este error, es posible que haya iniciado sesión con un perfil temporal. Cierre la sesión y vuelva a iniciarla e intente la operación de nuevo.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_IN_USE</strong></td>
<td>0x80073D02</td>
<td>No se pudo instalar el paquete porque los recursos modificados están actualmente en uso.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RECOVERY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D03</td>
<td>No se pudo recuperar el paquete porque los datos necesarios para la recuperación están dañados.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INVALID_</strong><br/> <strong>STAGED_SIGNATURE</strong><br/></td>
<td>0x80073D04</td>
<td>La firma no es válida. Para registrarse en modo de desarrollador, AppxSignature. p7x y AppxBlockMap.xml deben ser válidos o no deben estar presentes.<br/> Si es un desarrollador que usa F5 con Visual Studio, asegúrese de que el directorio de proyecto creado no contiene archivos de asignación de firma o bloque de las versiones anteriores del paquete.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DELETING_EXISTING_</strong><br/> <strong>APPLICATIONDATA_STORE_FAILED</strong><br/></td>
<td>0x80073D05</td>
<td>Se produjo un error al eliminar los datos de aplicación existentes anteriormente del paquete.<br/> Puede obtener este error si el <a href="/previous-versions/hh441475(v=vs.110)">simulador</a> se está ejecutando. Cierre el simulador. También puede obtener este error si hay archivos abiertos en los datos de la aplicación (por ejemplo, si tiene un archivo de registro abierto en un editor de texto).<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PACKAGE_DOWNGRADE</strong><br/></td>
<td>0x80073D06</td>
<td>No se pudo instalar el paquete porque ya hay instalada una versión superior de este paquete.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SYSTEM_</strong><br/> <strong>NEEDS_REMEDIATION</strong><br/></td>
<td>0x80073D07</td>
<td>Se detectó un error en un archivo binario del sistema. Para solucionar el problema, intente actualizar el equipo. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_INTEGRITY_</strong><br/> <strong>FAILURE_EXTERNAL</strong><br/></td>
<td>0x80073D08</td>
<td>Se detectó un binario dañado que no es de Windows en el sistema. <br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RESILIENCY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D09</td>
<td>No se pudo reanudar la operación porque los datos necesarios para la recuperación están dañados. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FIREWALL_</strong><br/> <strong>SERVICE_NOT_RUNNING</strong><br/></td>
<td>0x80073D0A</td>
<td>No se pudo instalar el paquete porque el servicio Firewall de Windows no se está ejecutando. Habilite el servicio Firewall de Windows e inténtelo de nuevo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_FAILED</strong></td>
<td>0x80073D0B</td>
<td>Error en la operación de movimiento del paquete.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>NOT_EMPTY</strong><br/></td>
<td>0x80073D0C</td>
<td>No se pudo realizar la operación de implementación porque el volumen no está vacío.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>N</strong><br/></td>
<td>0x80073D0D</td>
<td>No se pudo realizar la operación de implementación porque el volumen está sin conexión. En el caso de una actualización del paquete, el volumen hace referencia al volumen instalado de todas las versiones del paquete.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>CORRUPCIÓN</strong><br/></td>
<td>0x80073D0E</td>
<td>No se pudo realizar la operación de implementación porque el volumen especificado está dañado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REGISTRATION</strong><br/> <strong></strong><br/></td>
<td>0x80073D0F</td>
<td>No se pudo realizar la operación de implementación porque primero es necesario registrar la aplicación especificada.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_WRONG_</strong><br/> <strong>PROCESSOR_ARCHITECTURE</strong><br/></td>
<td>0x80073D10</td>
<td>No se pudo realizar la operación de implementación porque el paquete tiene como destino la arquitectura de procesador incorrecta.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEV_SIDELOAD_</strong><br/> <strong>LIMIT_EXCEEDED</strong><br/></td>
<td>0x80073D11</td>
<td>Ha alcanzado el número máximo de paquetes de instalación de prueba de desarrollador permitidos en este dispositivo. Desinstale un paquete de instalación de prueba y vuelva a intentarlo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_</strong><br/> <strong>MAIN_PACKAGE</strong><br/></td>
<td>0x80073D12</td>
<td>Se requiere un paquete de aplicación principal para instalar este paquete opcional. Instale primero el paquete principal e inténtelo de nuevo.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_NOT_</strong><br/> <strong>SUPPORTED_ON_FILESYSTEM</strong><br/></td>
<td>0x80073D13</td>
<td>Este tipo de paquete de aplicación no es compatible con este sistema de archivos.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_</strong><br/> <strong>BLOCKED_BY_STREAMING</strong><br/></td>
<td>0x80073D14</td>
<td>La operación de movimiento de paquetes se bloquea hasta que la aplicación haya finalizado el streaming.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_APPLICATIONID_</strong><br/> <strong>NOT_UNIQUE</strong><br/></td>
<td>0x80073D15</td>
<td>Un paquete de aplicación principal u otro opcional tiene el mismo identificador de aplicación que este paquete opcional. Cambie el identificador de la aplicación para el paquete opcional para evitar conflictos.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_STAGING_</strong><br/> <strong>ONHOLD</strong><br/></td>
<td>0x80073D16</td>
<td>Esta sesión de ensayo se ha mantenido para permitir la priorización de otra operación de almacenamiento provisional.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>RELATED_SET_UPDATE</strong><br/></td>
<td>0x80073D17</td>
<td>No se puede actualizar un conjunto relacionado porque el conjunto actualizado no es válido. Todos los paquetes del conjunto relacionado deben actualizarse al mismo tiempo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D18</td>
<td>Un paquete opcional con un punto de entrada FullTrust requiere que el paquete principal tenga la funcionalidad <strong>runFullTrust</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_USER_LOG_OFF</strong><br/></td>
<td>0x80073D19</td>
<td>Error al cerrar la sesión de un usuario.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PROVISION_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_PROVISIONED</strong><br/></td>
<td>0x80073D1A</td>
<td>Un aprovisionamiento de paquetes opcional requiere que el paquete principal de dependencia también esté aprovisionado.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_FAILED</strong><br/></td>
<td>0x80073D1B</td>
<td>No se pudo <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">comprobar la reputación de SmartScreen</a>en los paquetes.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_TIMEDOUT</strong><br/></td>
<td>0x80073D1C</td>
<td>Se agotó el tiempo de espera de la operación de <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">comprobación de reputación de SmartScreen</a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_OPTION_</strong><br/> <strong>NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1D</td>
<td>No se admite la opción de implementación actual.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPINSTALLER_</strong><br/> <strong>ACTIVATION_BLOCKED</strong><br/></td>
<td>0x80073D1E</td>
<td>La activación está bloqueada debido a la configuración de actualización. AppInstaller para esta aplicación.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REGISTRATION_FROM_</strong><br/> <strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1F</td>
<td>No se admiten las unidades remotas. Use <strong> \\ servidor\recurso compartido</strong> para registrar un paquete remoto.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_RAW_</strong><br/> <strong>DATA_WRITE_FAILED</strong><br/></td>
<td>0x80073D20</td>
<td>No se pudieron procesar y escribir los datos del paquete descargado en el disco.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_PACKAGE</strong><br/></td>
<td>0x80073D21</td>
<td>La operación de implementación se bloqueó debido a una directiva de familia por paquete que restringe las implementaciones en un volumen que no es del sistema. Por directiva, esta aplicación debe instalarse en la unidad del sistema, pero no se establece como el valor predeterminado. En configuración de almacenamiento, haga que la unidad del sistema sea la ubicación predeterminada para guardar el nuevo contenido y, a continuación, vuelva a intentar la instalación.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_MACHINE</strong><br/></td>
<td>0x80073D22</td>
<td>La operación de implementación se bloqueó debido a que una directiva de todo el equipo restringe las implementaciones en un volumen que no es del sistema. Por directiva, esta aplicación debe instalarse en la unidad del sistema, pero no se establece como el valor predeterminado. En configuración de almacenamiento, haga que la unidad del sistema sea la ubicación predeterminada para guardar el nuevo contenido y, a continuación, vuelva a intentar la instalación.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_PROFILE_POLICY</strong><br/></td>
<td>0x80073D23</td>
<td>La operación de implementación se bloqueó porque no se permite una implementación de perfil especial (los perfiles especiales son perfiles de usuario en los que se descartan los cambios después de que el usuario cierra la sesión). Intente iniciar sesión en una cuenta que no sea un perfil especial. Puede intentar cerrar la sesión y volver a iniciarla en la cuenta actual, o bien intentar iniciar sesión en una cuenta diferente.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_FAILED_</strong><br/> <strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br/> <strong>Active</strong><br/></td>
<td>0x80073D24</td>
<td>No se pudo realizar la operación de implementación debido a un <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">Directorio de paquetes mutable</a>de un paquete conflictivo. Para instalar este paquete, quite el paquete existente con el directorio de paquetes mutables en conflicto.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SINGLETON_RESOURCE_</strong><br/> <strong>INSTALLED_IN_ACTIVE_USER</strong><br/></td>
<td>0x80073D25</td>
<td>No se pudo instalar el paquete porque se especificó un recurso singleton y otro usuario con ese paquete instalado inició sesión. Asegúrese de que todos los usuarios activos con el paquete instalado estén desconectados y vuelva a intentar la instalación.<br/></td>
</tr>
<tr class="even">
<td>ERROR_DIFFERENT_VERSION_<strong></strong><br/> <strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br/></td>
<td>0x80073D26</td>
<td>Error en la instalación del paquete porque hay instalada una versión diferente del servicio. Intente instalar una versión más reciente del paquete.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SERVICE_EXISTS_</strong><br/> <strong>AS_NON_PACKAGED_SERVICE</strong><br/></td>
<td>0x80073D27</td>
<td>Error en la instalación del paquete porque existe una versión del servicio fuera de un paquete. msix/. appx. Póngase en contacto con su proveedor de software.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGED_SERVICE_</strong><br/> <strong>REQUIRES_ADMIN_PRIVILEGES</strong><br/></td>
<td>0x80073D28</td>
<td>No se pudo instalar el paquete porque se necesitan privilegios de administrador. Póngase en contacto con un administrador para instalar este paquete.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REDIRECTION_TO_</strong><br/> <strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br/></td>
<td>0x80073D29</td>
<td>Se produjo un error en la implementación del paquete porque la operación se habría redirigido a la cuenta predeterminada, cuando el autor de la llamada dijo que no lo haga.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_LACKS_</strong><br/> <strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br/></td>
<td>0x80073D2A</td>
<td>No se pudo implementar el paquete porque el paquete requiere una funcionalidad para establecer como destino de forma nativa este host.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_CONTENT</strong><br/></td>
<td>0x80073D2B</td>
<td>No se pudo implementar el paquete porque su contenido no es válido para un paquete sin firmar.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2C</td>
<td>No se pudo implementar el paquete porque su publicador no está en el espacio de nombres sin firmar.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2D</td>
<td>No se pudo implementar el paquete porque su publicador no está en el espacio de nombres firmado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_EXTERNAL_</strong><br/> <strong>LOCATION_NOT_ALLOWED</strong><br/></td>
<td>0x80073D2E</td>
<td>No se pudo implementar el paquete porque su publicador no está en el espacio de nombres firmado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FULLTRUST_</strong><br/> <strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D2F</td>
<td>Una dependencia de tiempo de ejecución de host que se resuelve en un paquete con contenido de plena confianza requiere que el paquete principal tenga la funcionalidad <strong>runFullTrust</strong> .<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_PACKAGING_INTERNAL</strong></td>
<td>0x80080200</td>
<td>La API de empaquetado encontró un error interno.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INTERLEAVING_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080201</td>
<td>El paquete no es válido porque su contenido está intercalado.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RELATIONSHIPS_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080202</td>
<td>El paquete no es válido porque contiene relaciones OPC.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_MISSING_</strong><br/> <strong>REQUIRED_FILE</strong><br/></td>
<td>0x80080203</td>
<td>El paquete no es válido porque falta un manifiesto o una asignación de bloque, o bien hay un archivo de integridad de código, pero falta un archivo de signatura.<br/> Asegúrese de que el paquete no tiene uno o varios de estos archivos necesarios:<br/>
<ul>
<li>\AppxManifest.xml</li>
<li>\AppxBlockMap.xml</li>
</ul>
Si el paquete contiene \AppxMetadata\CodeIntegrity.cat, también debe contener \AppxSignature.p7x.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_MANIFEST</strong></td>
<td>0x80080204</td>
<td>El archivo de AppxManifest.xml del paquete no es válido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_BLOCKMAP</strong></td>
<td>0x80080205</td>
<td>El archivo de AppxBlockMap.xml del paquete no es válido.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_CORRUPT_CONTENT</strong></td>
<td>0x80080206</td>
<td>No se puede leer el contenido del paquete porque está dañado.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_BLOCK_</strong><br/> <strong>HASH_INVALID</strong><br/></td>
<td>0x80080207</td>
<td>El valor hash calculado del bloque no coincide con el valor que tiene almacenado en la asignación de bloques.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_REQUESTED_</strong><br/> <strong>RANGE_TOO_LARGE</strong><br/></td>
<td>0x80080208</td>
<td>El intervalo de bytes solicitado es superior a 4 GB cuando se traduce a un intervalo de bytes de bloques.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUST_E_NOSIGNATURE</strong></td>
<td>0x800B0100</td>
<td>No hay ninguna firma presente en el asunto.<br/> Este error puede aparecer si el paquete no está firmado o la firma no es válida. El paquete debe estar firmado para implementarse.<br/></td>
</tr>
<tr class="odd">
<td><strong>CERT_E_UNTRUSTEDROOT</strong></td>
<td>0x800B0109</td>
<td>Una cadena de certificados procesada, pero termina en un certificado raíz que no es de confianza para el proveedor de confianza.<br/> Vea <a href="/previous-versions/br230260(v=vs.110)">firmar un paquete</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>CERT_E_CHAINING</strong></td>
<td>0x800B010A</td>
<td>No se pudo crear una cadena de certificados en una entidad de certificación raíz de confianza.<br/> Vea <a href="/previous-versions/br230260(v=vs.110)">firmar un paquete</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>SIP_CLIENT_DATA</strong> <br/></td>
<td>0x80080209</td>
<td>La estructura de <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>utilizada para firmar el paquete no contiene los datos necesarios<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>KEY_INFO</strong> <br/></td>
<td>0x8008020A</td>
<td>La estructura de <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> utilizada para cifrar o descifrar el paquete contiene datos no válidos.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>CONTENTGROUPMAP</strong><br/></td>
<td>0x8008020B</td>
<td>El mapa del grupo de contenido del paquete. msix/. appx no es válido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>APPINSTALLER</strong><br/></td>
<td>0x8008020C</td>
<td>El <a href="/windows/msix/app-installer/app-installer-root">archivo. AppInstaller</a> para el paquete no es válido.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_DELTA_BASELINE_</strong><br/> <strong>VERSION_MISMATCH</strong><br/></td>
<td>0x8008020D</td>
<td>La versión del paquete de línea de base en el paquete Delta no coincide con la versión del paquete de base de referencia que se va a actualizar.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_PACKAGE_</strong><br/> <strong>MISSING_FILE</strong><br/></td>
<td>0x8008020E</td>
<td>Falta un archivo en el paquete Delta del paquete actualizado.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>DELTA_PACKAGE</strong><br/></td>
<td>0x8008020F</td>
<td>El paquete Delta no es válido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_APPENDED_</strong><br/> <strong>PACKAGE_NOT_ALLOWED</strong><br/></td>
<td>0x80080210</td>
<td>No se permite el paquete Delta anexado para la operación actual.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGING_LAYOUT</strong><br/></td>
<td>0x80080211</td>
<td>El archivo de diseño de empaquetado no es válido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGESIGNCONFIG</strong><br/></td>
<td>0x80080212</td>
<td>El archivo packageSignConfig no es válido.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RESOURCESPRI_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080213</td>
<td>No se permite el archivo resources. PRI cuando no hay elementos de recursos en el manifiesto del paquete.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_FILE_</strong><br/> <strong>COMPRESSION_MISMATCH</strong><br/></td>
<td>0x80080214</td>
<td>El estado de compresión del archivo en la línea base y el paquete actualizado no coincide.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PAYLOAD_PACKAGE_EXTENSION</strong><br/></td>
<td>0x80080215</td>
<td>No se permiten extensiones no. appx para paquetes de carga destinados a plataformas anteriores.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br/></td>
<td>0x80080216</td>
<td>El archivo encryptionExclusionFileList no es válido.<br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a>Las aplicaciones no se inician y sus nombres están atenuados

En un equipo basado en Windows 10, no se pueden iniciar algunas aplicaciones y los nombres de las aplicaciones aparecen atenuados.

![Algunos nombres de aplicaciones aparecen atenuados en el menú Inicio](./images/app-names-dimmed.png)

Al intentar abrir una aplicación seleccionando el nombre atenuado, puede recibir uno de los siguientes mensajes de error:

> Hay un problema con \<*application name*> . Póngase en contacto con el administrador del sistema para repararlo o reinstalarlo.  
> Error: esta aplicación no se puede abrir

Además, las siguientes entradas de eventos se registran en el registro "Microsoft-Windows-TWinUI/Operational" en **Applications and Services\Microsoft\Windows\Apps**:

> Nombre de registro: Microsoft-Windows-TWinUI/Operational  
> Origen: Microsoft-Windows-inmersivo-Shell  
> Fecha: <*fecha*>  
> ID. de evento: 5960  
> Categoría de tarea: (5960)  
> Nivel: error  
> Palabras clave:  
> Descripción:  
> La activación del Microsoft.BingNews_8wekyb3d8bbwe de la aplicación. AppexNews para Windows. El contrato de inicio se bloqueó con el error 0x80073CFC porque su paquete se encuentra en estado: modificado.  

### <a name="cause"></a>Causa

Este problema se produce porque se modificó la entrada del registro para el valor de estado del paquete correspondiente de la aplicación.

### <a name="resolution"></a>Solución

> [!WARNING]
> Pueden producirse problemas graves si modifica el registro de manera incorrecta mediante el Editor del Registro u otro método. Estos problemas pueden requerir que tenga que volver a instalar el sistema operativo. Microsoft no brinda ninguna garantía de que se puedan solucionar estos problemas. Modifique el registro bajo su responsabilidad.

Para corregir este problema:

1. Inicie el editor del registro y, a continuación, busque la subclave **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** .
2. Para hacer una copia de seguridad de los datos de la subclave, haga clic con el botón secundario en **PackageList**, seleccione **exportar** y, a continuación, guarde los datos como un archivo de registro.
3. Para cada una de las aplicaciones que se enumeran en las entradas de registro de ID. de evento 5960, siga estos pasos:  
   1. Busque la entrada **PackageStatus** .
   2. Establezca el valor de **PackageStatus** en cero (**0**).
   > [!NOTE]  
   > Si no hay ninguna entrada para la aplicación en **PackageList**, el problema tiene alguna otra causa. En el caso del evento de ejemplo de este artículo, la subclave completa es **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**
4. Reinicie el equipo.

## <a name="get-additional-help"></a>Obtener ayuda adicional

Si necesita más ayuda con la resolución de un problema que está experimentando al empaquetar, implementar o consultar un paquete de aplicación de Windows (. msix/. appx) como desarrollador, consulte estos recursos de soporte técnico para desarrolladores adicionales.

- [Microsoft Q&a](/answers/topics/uwp.html?filter=all&sort=active) ofrece respuestas pertinentes y oportunas a sus problemas técnicos de una comunidad de expertos y ingenieros de Microsoft.
- Para obtener ayuda de la comunidad con preguntas de desarrollo, existen nuestros [foros](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)y [stackoverflow](https://stackoverflow.com/questions).
- El sitio de [soporte técnico para desarrolladores de Windows](https://developer.microsoft.com/windows/support) explica otras opciones de soporte técnico.

## <a name="related-topics"></a>Temas relacionados

- [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Cómo firmar un paquete de la aplicación con SignTool)
- [Cómo solucionar errores de firma de paquete de aplicaciones](how-to-troubleshoot-app-package-signature-errors.md)
