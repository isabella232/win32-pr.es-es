---
title: Solución de problemas de empaquetado, implementación y consulta de aplicaciones de Windows
description: Use estas sugerencias para solucionar problemas que experimente al empaquetar, implementar o consultar un paquete de aplicación.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: ce602d4a65d0287154a9eee94665d025a628f6d8ce3a7f086700625820637a5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552322"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>Solución de problemas de empaquetado, implementación y consulta de aplicaciones de Windows

Use estas sugerencias para solucionar los problemas que experimenta al empaquetar, implementar o consultar un paquete de aplicación de Windows (.msix/.appx) como desarrollador.

> [!NOTE]
> Este artículo está destinado a desarrolladores. Si no es un desarrollador y busca ayuda con un error de Windows instalación de la aplicación, consulte Windows [soporte técnico.](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10)

## <a name="get-diagnostic-information"></a>Obtener información de diagnóstico

Cuando se produce un error en una API, devuelve un código de error que describe el problema. Si el código de error no proporciona suficiente información, encontrará más información de diagnóstico en los registros de eventos detallados.

Para acceder a los registros de eventos de empaquetado e **implementación Visor de eventos**, siga estos pasos:

1. Realice uno de estos pasos:

    * Haga **clic en** Iniciar en Windows menú, escriba **Visor de eventos** y **presione Entrar.**
    * Ejecute **eventvwr.msc.**

2. En la página de la izquierda, expanda Visor de eventos registros de servicios y aplicaciones **(locales)**  >    >  **de Microsoft**  >  **Windows**.
3. Compruebe los registros disponibles en estas categorías:

    * **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**
    * **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**

Para empezar, busque los registros en **AppXDeployment-Server**. Si el error fue causado **por** 0x80073CF0 o **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, puede haber detalles adicionales en los registros **de AppxpackagingOM.**

También puede usar el [comando Get-AppxLog](/powershell/module/appx/get-appxlog) en PowerShell para obtener los primeros eventos registrados. En el ejemplo siguiente se muestran los registros asociados a la operación de implementación más reciente.

```PowerShell
Get-Appxlog
```

En el ejemplo siguiente se muestran los registros asociados a la operación de implementación más reciente en una tabla interactiva en una ventana independiente.

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>Códigos comunes de error

En esta tabla se enumeran algunos de los códigos de error más comunes. Si necesita más ayuda con uno de estos errores, o si encuentra un código de error que no está en esta lista, vea opciones [de ayuda adicionales](#get-additional-help).

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
<th>Descripción y posibles causas</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><strong>E_FILENOTFOUND</strong></td>
<td>0x80070002</td>
<td>El archivo o la ruta de acceso no se encuentra. Esto puede ocurrir durante una validación de la lista de tipos COM requiere que la ruta de acceso del directorio exista realmente en el paquete MSIX.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_BAD_FORMAT</strong></td>
<td>0x8007000B</td>
<td>El paquete no tiene el formato correcto y es necesario volver a crearlo o volver a firmarlo.<br/> Este error puede producirse si hay una discrepancia entre el nombre del firmando del firmando y el nombre AppxManifest.xml publicador.<br/> Consulte <a href="how-to-sign-a-package-using-signtool.md">Cómo firmar un paquete de aplicación mediante SignTool.</a><br/></td>
</tr>
<tr class="even">
<td><strong>E_INVALIDARG</strong></td>
<td>0x80070057</td>
<td>Uno o varios argumentos no son válidos. Si comprueba el registro de eventos de AppXDeployment-Server y ve el siguiente evento: "Al instalar el paquete, el sistema no pudo registrar la extensión windows.repositoryExtension debido al siguiente error: El parámetro es incorrecto". <br/> Puede obtener este error si los elementos de manifiesto DisplayName o Description contienen caracteres no permitidos por Windows firewall; es |  y todos , debido a Windows no se puede crear el perfil de AppContainer para el paquete. Quite estos caracteres del manifiesto e intente instalar el paquete. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPEN_</strong><br/> <strong>PACKAGE_FAILED</strong><br/></td>
<td>0x80073CF0</td>
<td>No se pudo abrir el paquete.<br/> Causas posibles:<br/>
<ul>
<li>El paquete no está firmado.</li>
<li>El nombre del publicador no coincide con el asunto del certificado de firma.</li>
<li>Falta file:// prefijo o no se pudo encontrar el paquete en la ubicación especificada.</li>
</ul>
Para más información, consulte el registro de eventos <strong>AppxPackagingOM.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_PACKAGE_</strong><br/> <strong>NOT_FOUND</strong><br/></td>
<td>0x80073CF1</td>
<td>No se encontró el paquete.<br/> Es posible que reciba este error al quitar un paquete que no está instalado para el usuario actual.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>Paquete</strong><br/></td>
<td>0x80073CF2</td>
<td>Los datos del paquete no son válidos.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_RESOLVE_</strong><br/> <strong>DEPENDENCY_FAILED</strong><br/></td>
<td>0x80073CF3</td>
<td>Error de actualización, dependencia o validación de conflicto en el paquete.<br/> Causas posibles:<br/>
<ul>
<li>El paquete entrante entra en conflicto con un paquete instalado.</li>
<li>No se encuentra una dependencia de paquete especificada.</li>
<li>El paquete no admite la arquitectura de procesador correcta.</li>
</ul>
Para más información, consulte el registro de eventos <strong>AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OUT_</strong><br/> <strong>OF_DISK_SPACE</strong><br/></td>
<td>0x80073CF4</td>
<td>No hay suficiente espacio en disco en el equipo. Liberar espacio e intentarlo de nuevo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_NETWORK_</strong><br/> <strong>Fracaso</strong><br/></td>
<td>0x80073CF5</td>
<td>No se puede descargar el paquete.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>REGISTRATION_FAILURE</strong><br/></td>
<td>0x80073CF6</td>
<td>El paquete no se puede registrar.<br/> Para más información, consulte el registro de eventos <strong>AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>DEREGISTRATION_EFAILURE</strong><br/></td>
<td>0x80073CF7</td>
<td>No se puede anular el registro del paquete.<br/> Es posible que reciba este error al quitar un paquete.<br/> Para más información, consulte el registro de eventos <strong>AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_CANCEL</strong></td>
<td>0x80073CF8</td>
<td>El usuario canceló la solicitud de instalación.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_FAILED</strong></td>
<td>0x80073CF9</td>
<td>Error de instalación del paquete. Póngase en contacto con el proveedor de software.<br/> Para más información, consulte el registro de eventos <strong>AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_REMOVE_FAILED</strong></td>
<td>0x80073CFA</td>
<td>Error de eliminación del paquete.<br/> Puede recibir este error en caso de errores que se producen durante la desinstalación del paquete.<br/> Para obtener más información, <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>vea RemovePackageAsync.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>ALREADY_EXISTS</strong><br/></td>
<td>0x80073CFB</td>
<td>El paquete suministrado ya está instalado y se ha bloqueado la reinstalación del paquete. <br/> Puede recibir este error si instala un paquete que no es bit a bit idéntico al paquete que ya está instalado. Tenga en cuenta que la firma digital también forma parte del paquete. Por lo tanto, si un paquete se vuelve a generar o resigna, ya no es idéntico bit a bit al paquete instalado previamente. Dos opciones posibles para corregir este error son: (1) Incrementar el número de versión de la aplicación y, a continuación, recompilar y volver asign el paquete (2) Quitar el paquete antiguo para todos los usuarios del sistema antes de instalar el nuevo paquete. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REMEDIATION</strong></td>
<td>0x80073CFC</td>
<td>No se puede iniciar la aplicación. Pruebe a reinstalar la aplicación.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PREREQUISITE_FAILED</strong><br/></td>
<td>0x80073CFD</td>
<td>No se pudo cumplir un requisito previo de instalación especificado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>REPOSITORY_CORRUPTED</strong><br/></td>
<td>0x80073CFE</td>
<td>El repositorio de paquetes está dañado.<br/> Puede recibir este error si la carpeta a la que hace referencia esta clave del Registro no existe o está dañada: <br/> <strong>HKLM\Software\Microsoft\Windows\</strong><br/> <strong>CurrentVersion\Appx\PackageRepositoryRoot</strong><br/> Para recuperarse de este estado, actualice el equipo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>POLICY_FAILURE</strong><br/></td>
<td>0x80073CFF</td>
<td>Para instalar esta aplicación, necesita una licencia de desarrollador o un sistema habilitado para la instalación de instalación local. <br/> Puede recibir este error si el paquete no cumple uno de los siguientes requisitos:<br/>
<ul>
<li>La aplicación se implementa mediante F5 en Visual Studio en un equipo con una licencia Windows desarrollador.</li>
<li>El paquete se firma con una firma de Microsoft y se implementa como parte de Windows o desde el Microsoft Store.</li>
<li>El paquete se firma con una firma de confianza y se instala en un equipo con una licencia de desarrollador, un equipo unido a un dominio con la directiva AllowAllTrustedApps habilitada o un equipo con una licencia de instalación local de Windows con la directiva AllowAllTrustedApps habilitada.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_UPDATING</strong></td>
<td>0x80073D00</td>
<td>La aplicación no se puede iniciar porque se está actualizando actualmente.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_</strong><br/> <strong>BLOCKED_BY_POLICY</strong><br/></td>
<td>0x80073D01</td>
<td>La directiva bloquea la operación de implementación de paquetes. Póngase en contacto con el administrador del sistema.<br/> Causas posibles:<br/>
<ul>
<li>Las directivas de control de aplicaciones bloquean la implementación de paquetes.</li>
<li>La directiva Permitir operaciones de implementación en perfiles especiales bloquea la &quot; implementación de &quot; paquetes.</li>
</ul>
Una de las posibles razones es la necesidad de un perfil móvil. Para obtener información sobre cómo configurar perfiles de usuario móviles en cuentas de usuario, vea <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Implementar perfiles de usuario móviles.</a> Si no hay directivas configuradas en el sistema y todavía ve este error, quizás haya iniciado sesión con un perfil temporal. Cierre la sesión e inicie sesión de nuevo y vuelva a intentar la operación.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_IN_USE</strong></td>
<td>0x80073D02</td>
<td>No se pudo instalar el paquete porque los recursos que modifica están actualmente en uso.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RECOVERY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D03</td>
<td>No se pudo recuperar el paquete porque los datos necesarios para la recuperación están dañados.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INVALID_</strong><br/> <strong>STAGED_SIGNATURE</strong><br/></td>
<td>0x80073D04</td>
<td>La firma no es válida. Para registrarse en modo de desarrollador, AppxSignature.p7x y AppxBlockMap.xml deben ser válidos o no deben estar presentes.<br/> Si es un desarrollador que usa F5 con Visual Studio, asegúrese de que el directorio del proyecto creado no contiene archivos de asignación de firma o de bloque de versiones anteriores del paquete.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DELETING_EXISTING_</strong><br/> <strong>APPLICATIONDATA_STORE_FAILED</strong><br/></td>
<td>0x80073D05</td>
<td>Error al eliminar los datos de aplicación existentes anteriormente del paquete.<br/> Puede obtener este error si el <a href="/previous-versions/hh441475(v=vs.110)">simulador</a> se está ejecutando. Cierre el simulador. También puede obtener este error si hay archivos abiertos en los datos de la aplicación (por ejemplo, si tiene un archivo de registro abierto en un editor de texto).<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PACKAGE_DOWNGRADE</strong><br/></td>
<td>0x80073D06</td>
<td>No se pudo instalar el paquete porque ya está instalada una versión superior de este paquete.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SYSTEM_</strong><br/> <strong>NEEDS_REMEDIATION</strong><br/></td>
<td>0x80073D07</td>
<td>Se detectó un error en un binario del sistema. Para corregir el problema, intente actualizar el equipo. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_INTEGRITY_</strong><br/> <strong>FAILURE_EXTERNAL</strong><br/></td>
<td>0x80073D08</td>
<td>Se detectó un binario Windows no dañado en el sistema. <br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RESILIENCY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D09</td>
<td>No se pudo reanudar la operación porque los datos necesarios para la recuperación están dañados. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FIREWALL_</strong><br/> <strong>SERVICE_NOT_RUNNING</strong><br/></td>
<td>0x80073D0A</td>
<td>No se pudo instalar el paquete porque el Windows firewall no se está ejecutando. Habilite el servicio Windows Firewall e inténtelo de nuevo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_FAILED</strong></td>
<td>0x80073D0B</td>
<td>Error en la operación de traslado del paquete.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>NOT_EMPTY</strong><br/></td>
<td>0x80073D0C</td>
<td>Error en la operación de implementación porque el volumen no está vacío.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>sin conexión</strong><br/></td>
<td>0x80073D0D</td>
<td>Error en la operación de implementación porque el volumen está sin conexión. Para una actualización de paquete, el volumen hace referencia al volumen instalado de todas las versiones del paquete.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>Corrupto</strong><br/></td>
<td>0x80073D0E</td>
<td>Error en la operación de implementación porque el volumen especificado está dañado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REGISTRATION</strong><br/> <strong></strong><br/></td>
<td>0x80073D0F</td>
<td>Error en la operación de implementación porque la aplicación especificada debe registrarse primero.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_WRONG_</strong><br/> <strong>PROCESSOR_ARCHITECTURE</strong><br/></td>
<td>0x80073D10</td>
<td>Error en la operación de implementación porque el paquete tiene como destino la arquitectura de procesador incorrecta.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEV_SIDELOAD_</strong><br/> <strong>LIMIT_EXCEEDED</strong><br/></td>
<td>0x80073D11</td>
<td>Ha alcanzado el número máximo de paquetes de instalación local del desarrollador permitidos en este dispositivo. Desinstale un paquete descargado localmente e inténtelo de nuevo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_</strong><br/> <strong>MAIN_PACKAGE</strong><br/></td>
<td>0x80073D12</td>
<td>Se requiere un paquete de aplicación principal para instalar este paquete opcional. Instale primero el paquete principal e inténtelo de nuevo.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_NOT_</strong><br/> <strong>SUPPORTED_ON_FILESYSTEM</strong><br/></td>
<td>0x80073D13</td>
<td>Este tipo de paquete de aplicación no se admite en este sistema de archivos.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_</strong><br/> <strong>BLOCKED_BY_STREAMING</strong><br/></td>
<td>0x80073D14</td>
<td>La operación de movimiento de paquetes se bloquea hasta que la aplicación ha finalizado el streaming.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_APPLICATIONID_</strong><br/> <strong>NOT_UNIQUE</strong><br/></td>
<td>0x80073D15</td>
<td>Un paquete de aplicación principal u otro opcional tiene el mismo identificador de aplicación que este paquete opcional. Cambie el identificador de aplicación del paquete opcional para evitar conflictos.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_STAGING_</strong><br/> <strong>ONHOLD</strong><br/></td>
<td>0x80073D16</td>
<td>Esta sesión de almacenamiento provisional se ha mantenido para permitir que se dé prioridad a otra operación de almacenamiento provisional.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>RELATED_SET_UPDATE</strong><br/></td>
<td>0x80073D17</td>
<td>No se puede actualizar un conjunto relacionado porque el conjunto actualizado no es válido. Todos los paquetes del conjunto relacionado deben actualizarse al mismo tiempo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D18</td>
<td>Un paquete opcional con un punto de entrada FullTrust requiere que el paquete principal tenga <strong>la funcionalidad runFullTrust.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_USER_LOG_OFF</strong><br/></td>
<td>0x80073D19</td>
<td>Se produjo un error porque se ha cerrado la sesión de un usuario.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PROVISION_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_PROVISIONED</strong><br/></td>
<td>0x80073D1A</td>
<td>Un aprovisionamiento de paquete opcional requiere que también se aprovisione el paquete principal de dependencia.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_FAILED</strong><br/></td>
<td>0x80073D1B</td>
<td>Los paquetes no pudieron comprobar <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">la reputación de SmartScreen.</a><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_TIMEDOUT</strong><br/></td>
<td>0x80073D1C</td>
<td>Se ha pasado el tiempo de espera de la operación de comprobación de reputación de <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen.</a><br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_OPTION_</strong><br/> <strong>NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1D</td>
<td>No se admite la opción de implementación actual.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPINSTALLER_</strong><br/> <strong>ACTIVATION_BLOCKED</strong><br/></td>
<td>0x80073D1E</td>
<td>La activación está bloqueada debido a la configuración de actualización de .appinstaller para esta aplicación.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REGISTRATION_FROM_</strong><br/> <strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1F</td>
<td>No se admiten unidades remotas. Use <strong> \\ server\share</strong> para registrar un paquete remoto.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_RAW_</strong><br/> <strong>DATA_WRITE_FAILED</strong><br/></td>
<td>0x80073D20</td>
<td>No se pudieron procesar y escribir datos de paquetes descargados en el disco.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_PACKAGE</strong><br/></td>
<td>0x80073D21</td>
<td>La operación de implementación se bloqueó debido a una directiva por familia de paquetes que restringe las implementaciones en un volumen que no es del sistema. Por directiva, esta aplicación debe instalarse en la unidad del sistema, pero no se establece como valor predeterminado. En Storage configuración, haga que la unidad del sistema sea la ubicación predeterminada para guardar el nuevo contenido y, a continuación, vuelva a intentar la instalación.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_MACHINE</strong><br/></td>
<td>0x80073D22</td>
<td>La operación de implementación se bloqueó debido a una directiva de todo el equipo que restringe las implementaciones en un volumen que no es del sistema. Por directiva, esta aplicación debe instalarse en la unidad del sistema, pero no se establece como valor predeterminado. En Storage configuración, haga que la unidad del sistema sea la ubicación predeterminada para guardar el nuevo contenido y, a continuación, vuelva a intentar la instalación.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_PROFILE_POLICY</strong><br/></td>
<td>0x80073D23</td>
<td>La operación de implementación se bloqueó porque no se permite la implementación de perfiles especiales (los perfiles especiales son perfiles de usuario donde los cambios se descartan después de que el usuario cierra la sesión). Intente iniciar sesión en una cuenta que no sea un perfil especial. Puede intentar cerrar sesión y volver a iniciar sesión en la cuenta actual, o intentar iniciar sesión en otra cuenta.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_FAILED_</strong><br/> <strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br/> <strong>Directorio</strong><br/></td>
<td>0x80073D24</td>
<td>Error en la operación de implementación debido a un directorio de paquete <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">mutable de un paquete en conflicto.</a> Para instalar este paquete, quite el paquete existente con el directorio de paquete mutable en conflicto.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SINGLETON_RESOURCE_</strong><br/> <strong>INSTALLED_IN_ACTIVE_USER</strong><br/></td>
<td>0x80073D25</td>
<td>Error en la instalación del paquete porque se especificó un recurso singleton y otro usuario con ese paquete instalado ha iniciado sesión. Asegúrese de que todos los usuarios activos con el paquete instalado hayan cerrado sesión y vuelva a intentar la instalación.<br/></td>
</tr>
<tr class="even">
<td>ERROR_DIFFERENT_VERSION_<strong></strong><br/> <strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br/></td>
<td>0x80073D26</td>
<td>Error en la instalación del paquete porque hay instalada una versión diferente del servicio. Intente instalar una versión más reciente del paquete.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SERVICE_EXISTS_</strong><br/> <strong>AS_NON_PACKAGED_SERVICE</strong><br/></td>
<td>0x80073D27</td>
<td>Error en la instalación del paquete porque existe una versión del servicio fuera de un paquete .msix/.appx. Póngase en contacto con su proveedor de software.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGED_SERVICE_</strong><br/> <strong>REQUIRES_ADMIN_PRIVILEGES</strong><br/></td>
<td>0x80073D28</td>
<td>Error en la instalación del paquete porque se requieren privilegios de administrador. Póngase en contacto con un administrador para instalar este paquete.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REDIRECTION_TO_</strong><br/> <strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br/></td>
<td>0x80073D29</td>
<td>Error en la implementación del paquete porque la operación se habría redirigido a la cuenta predeterminada, cuando el autor de la llamada le indicó que no lo haría.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_LACKS_</strong><br/> <strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br/></td>
<td>0x80073D2A</td>
<td>Error en la implementación del paquete porque el paquete requiere una capacidad para dirigirse de forma nativa a este host.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_CONTENT</strong><br/></td>
<td>0x80073D2B</td>
<td>Error en la implementación del paquete porque su contenido no es válido para un paquete sin signo.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2C</td>
<td>Error en la implementación del paquete porque su publicador no está en el espacio de nombres sin signo.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2D</td>
<td>Error en la implementación del paquete porque su publicador no está en el espacio de nombres firmado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_EXTERNAL_</strong><br/> <strong>LOCATION_NOT_ALLOWED</strong><br/></td>
<td>0x80073D2E</td>
<td>Error en la implementación del paquete porque su publicador no está en el espacio de nombres firmado.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FULLTRUST_</strong><br/> <strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D2F</td>
<td>Una dependencia en tiempo de ejecución de host que se resuelve en un paquete con contenido de plena confianza requiere que el paquete principal tenga <strong>la funcionalidad runFullTrust.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_PACKAGING_INTERNAL</strong></td>
<td>0x80080200</td>
<td>La API de empaquetado ha detectado un error interno.<br/></td>
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
<td>El paquete no es válido porque falta un manifiesto o un mapa de bloques, o porque hay un archivo de integridad de código, pero falta un archivo de firma.<br/> Asegúrese de que al paquete no le faltan uno o varios de estos archivos necesarios:<br/>
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
<td>El contenido del paquete no se puede leer porque está dañado.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_BLOCK_</strong><br/> <strong>HASH_INVALID</strong><br/></td>
<td>0x80080207</td>
<td>El valor hash calculado del bloque no coincide con el valor has almacenado en el mapa de bloques.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_REQUESTED_</strong><br/> <strong>RANGE_TOO_LARGE</strong><br/></td>
<td>0x80080208</td>
<td>El intervalo de bytes solicitado es de más de 4 GB cuando se convierte en un intervalo de bytes de bloques.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUST_E_NOSIGNATURE</strong></td>
<td>0x800B0100</td>
<td>No hay ninguna firma en el asunto.<br/> Puede recibir este error si el paquete no tiene signo o la firma no es válida. El paquete debe estar firmado para implementarse.<br/></td>
</tr>
<tr class="odd">
<td><strong>CERT_E_UNTRUSTEDROOT</strong></td>
<td>0x800B0109</td>
<td>Una cadena de certificados procesada, pero terminada en un certificado raíz que no es de confianza para el proveedor de confianza.<br/> Consulte <a href="/previous-versions/br230260(v=vs.110)">Firma de un paquete.</a><br/></td>
</tr>
<tr class="even">
<td><strong>CERT_E_CHAINING</strong></td>
<td>0x800B010A</td>
<td>No se pudo crear una cadena de certificados para una entidad de certificación raíz de confianza.<br/> Consulte <a href="/previous-versions/br230260(v=vs.110)">Firma de un paquete.</a><br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>SIP_CLIENT_DATA</strong> <br/></td>
<td>0x80080209</td>
<td>La <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>utilizada para firmar el paquete no contenía los datos necesarios.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>KEY_INFO</strong> <br/></td>
<td>0x8008020A</td>
<td>La <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> que se usa para cifrar o descifrar el paquete contiene datos no válidos.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>CONTENTGROUPMAP</strong><br/></td>
<td>0x8008020B</td>
<td>El mapa del grupo de contenido del paquete .msix/.appx no es válido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>Appinstaller</strong><br/></td>
<td>0x8008020C</td>
<td>El <a href="/windows/msix/app-installer/app-installer-root">archivo .appinstaller</a> del paquete no es válido.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_DELTA_BASELINE_</strong><br/> <strong>VERSION_MISMATCH</strong><br/></td>
<td>0x8008020D</td>
<td>La versión del paquete de línea base del paquete delta no coincide con la versión del paquete de línea base que se va a actualizar.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_PACKAGE_</strong><br/> <strong>MISSING_FILE</strong><br/></td>
<td>0x8008020E</td>
<td>Al paquete delta le falta un archivo del paquete actualizado.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>DELTA_PACKAGE</strong><br/></td>
<td>0x8008020F</td>
<td>El paquete delta no es válido.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_APPENDED_</strong><br/> <strong>PACKAGE_NOT_ALLOWED</strong><br/></td>
<td>0x80080210</td>
<td>No se permite el paquete anexado diferencial para la operación actual.<br/></td>
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
<td>No se permite el archivo resources.pri cuando no hay elementos de recursos en el manifiesto del paquete.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_FILE_</strong><br/> <strong>COMPRESSION_MISMATCH</strong><br/></td>
<td>0x80080214</td>
<td>El estado de compresión del archivo en la línea base y el paquete actualizado no coincide.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PAYLOAD_PACKAGE_EXTENSION</strong><br/></td>
<td>0x80080215</td>
<td>No se permiten extensiones .appx que no sean para paquetes de carga que tienen como destino plataformas anteriores.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br/></td>
<td>0x80080216</td>
<td>El archivo encryptionExclusionFileList no es válido.<br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a>Las aplicaciones no se inician y sus nombres están atenuados

En un Windows 10 basado en aplicaciones, no puede iniciar algunas aplicaciones y los nombres de aplicación aparecen atenuados.

![Algunos nombres de aplicación aparecen atenuados en el menú Inicio](./images/app-names-dimmed.png)

Al intentar abrir una aplicación seleccionando el nombre atenuado, puede recibir uno de los siguientes mensajes de error:

> Hay un problema con \<*application name*> . Póngase en contacto con el administrador del sistema para repararlo o volver a instalarlo.  
> Error: Esta aplicación no se puede abrir

Además, las siguientes entradas de evento se registran en el registro "Microsoft-Windows-TWinUI/Operational" en **Aplicaciones y servicios\Microsoft\Windows\Apps**:

> Nombre del registro: Microsoft-Windows-TWinUI/Operational  
> Origen: Microsoft-Windows-Immersive-Shell  
> Fecha: <*fecha*>  
> Id. de evento: 5960  
> Categoría de tarea: (5960)  
> Nivel: Error  
> Palabras clave:  
> Descripción:  
> Activación de la aplicación Microsoft.BingNews_8wekyb3d8bbwe! AppexNews para el Windows. Se bloqueó el inicio del contrato con 0x80073CFC error porque su paquete está en estado: Modificado.  

### <a name="cause"></a>Causa

Este problema se produce porque se modificó la entrada del Registro para el valor de estado del paquete correspondiente de la aplicación.

### <a name="resolution"></a>Solución

> [!WARNING]
> Pueden producirse problemas graves si modifica el registro de manera incorrecta mediante el Editor del Registro u otro método. Estos problemas pueden requerir que tenga que volver a instalar el sistema operativo. Microsoft no brinda ninguna garantía de que se puedan solucionar estos problemas. Modifique el registro bajo su responsabilidad.

Para corregir este problema:

1. Inicie el Editor del Registro y, a continuación, **busqueHKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** subclave.
2. Para hacer una copia de seguridad de los datos de subclave, haga clic con el botón derecho en **PackageList**, seleccione **Exportar** y, a continuación, guarde los datos como un archivo del Registro.
3. Para cada una de las aplicaciones que aparecen en las entradas del registro de Id. de evento 5960, siga estos pasos:  
   1. Busque la **entrada PackageStatus.**
   2. Establezca el valor de **PackageStatus** en cero (**0**).
   > [!NOTE]  
   > Si no hay ninguna entrada para la aplicación en **PackageList**, el problema tiene otra causa. En el caso del evento de ejemplo de este artículo, la subclave completa **seHKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**
4. Reinicie el equipo.

## <a name="get-additional-help"></a>Obtener ayuda adicional

Si necesita más ayuda para resolver un problema que experimenta al empaquetar, implementar o consultar un paquete de aplicación de Windows (.msix/.appx) como desarrollador, consulte estos recursos de soporte técnico para desarrolladores adicionales.

- [Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) ofrece respuestas pertinentes y a tiempo a los problemas técnicos de una comunidad de expertos e ingenieros de Microsoft.
- Para obtener ayuda de la comunidad con preguntas de desarrollo, están [nuestros foros](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)y [StackOverflow.](https://stackoverflow.com/questions)
- El [Windows de soporte técnico para desarrolladores](https://developer.microsoft.com/windows/support) explica otras opciones de soporte técnico.

## <a name="related-topics"></a>Temas relacionados

- [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Cómo firmar un paquete de la aplicación con SignTool)
- [Solución de errores de firma de paquetes de aplicaciones](how-to-troubleshoot-app-package-signature-errors.md)
