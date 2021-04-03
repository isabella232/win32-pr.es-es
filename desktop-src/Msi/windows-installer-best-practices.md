---
description: 'En esta sección se enumera una lista de sugerencias, vinculadas a la documentación principal del SDK de Windows Installer, para ayudar a los desarrolladores de aplicaciones, los autores de la instalación, los profesionales de ti y los desarrolladores de infraestructura a detectar los procedimientos recomendados para usar el Windows Installer:'
ms.assetid: ff48d995-fe6f-4d1b-898d-67574ed3c5b7
title: Procedimientos recomendados de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffaf6aae83afbe510f2b1eefc447e34754296ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082921"
---
# <a name="windows-installer-best-practices"></a>Procedimientos recomendados de Windows Installer

En esta sección se enumera una lista de sugerencias, vinculadas a la documentación principal del SDK de Windows Installer, para ayudar a los desarrolladores de aplicaciones, los autores de la instalación, los profesionales de ti y los desarrolladores de infraestructura a detectar los procedimientos recomendados para usar el Windows Installer:

-   [Actualice la versión de Windows Installer.](#update-the-windows-installer-version)
-   [Cumplir los requisitos de certificación del logotipo de Windows.](#meet-the-windows-logo-certification-requirements)
-   [Preparar el paquete para la localización.](#prepare-the-package-for-localization)
-   [Actualice la documentación y las herramientas de desarrollo de Windows Installer.](#update-your-windows-installer-development-tools-and-documentation)
-   [Si decide volver a empaquetar una aplicación de instalación heredada, siga las prácticas recomendadas para el empaquetado.](#if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices)
-   [No intente reemplazar los recursos protegidos.](#do-not-try-to-replace-protected-resources)
-   [No dependa de recursos no críticos.](#do-not-depend-upon-non-critical-resources)
-   [Use la API para recuperar la información de configuración de Windows Installer.](#use-the-api-to-retrieve-windows-installer-configuration-information)
-   [Organice la instalación de la aplicación en torno a los componentes.](#organize-the-installation-of-your-application-around-components)
-   [Reduzca el tamaño de los paquetes de Windows Installer de gran tamaño.](#reduce-the-size-of-large-windows-installer-packages)
-   [Si usa acciones personalizadas, siga las prácticas recomendadas para acciones personalizadas.](#if-you-use-custom-actions-follow-good-custom-action-practices)
-   [Si utiliza ensamblados, siga las prácticas recomendadas para el ensamblado](#if-you-use-assemblies-follow-good-assembly-practices)
-   [No distribuir instalaciones simultáneas.](#do-not-ship-concurrent-installations)
-   [Mantener los nombres de paquete y los códigos de paquete coherentes.](#keep-package-names-and-package-codes-consistent)
-   [No utilice las tablas SelfReg y TypeLib.](#do-not-use-the-selfreg-and-typelib-tables)
-   [Proporcione la opción de instalación sin una interfaz de usuario.](#provide-the-option-to-install-without-a-user-interface)
-   [Evite el uso de la Directiva AlwaysInstallElevated.](#avoid-using-the-alwaysinstallelevated-policy)
-   [Habilite la Directiva DisableMedia para limitar la instalación no autorizada.](#enable-the-disablemedia-policy-to-limit-unauthorized-installation)
-   [Mantenga los archivos de origen del paquete original seguros y disponibles para los usuarios.](#keep-the-original-package-source-files-secure-and-available-to-users)
-   [Habilite el registro detallado en el equipo del usuario al solucionar problemas de implementación.](#enable-verbose-logging-on-users-computer-when-troubleshooting-deployment)
-   [La desinstalación deja el equipo del usuario en un estado limpio.](#uninstallation-leaves-the-users-computer-in-a-clean-state)
-   [Probar paquetes para la implementación de instalación por usuario y por equipo.](#test-packages-for-both-per-user-and-per-machine-installation-deployment)
-   [Planee y pruebe una estrategia de servicio antes de enviar la aplicación.](#plan-and-test-a-servicing-strategy-before-shipping-the-application)
-   [Reduzca la dependencia de las actualizaciones en los orígenes originales.](#reduce-the-dependency-of-updates-upon-the-original-sources)
-   [No distribuya módulos de combinación no redistribuibles.](#do-not-distribute-unserviceable-merge-modules)
-   [Evite aplicar revisiones a las instalaciones administrativas.](#avoid-patching-administrative-installations)
-   [Registra las actualizaciones para que se ejecuten con privilegios elevados.](#register-updates-to-run-with-elevated-privilege)
-   [Use la tabla MsiPatchSequence para secuenciar las revisiones.](#use-the-msipatchsequence-table-to-sequence-patches)
-   [Pruebe el paquete de instalación exhaustivamente.](#test-the-installation-package-thoroughly)
-   [Corrija todos los errores de validación antes de implementar un paquete de instalación nuevo o revisado.](#fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package)
-   [Cree una instalación segura.](#author-a-secure-installation)
-   [Usar PMSIHANDLE en lugar de HANDLE](#use-pmsihandle-instead-of-handle)

## <a name="update-the-windows-installer-version"></a>Actualice la versión de Windows Installer.

-   Use Windows Installer 5,0 en Windows Server 2008 R2 y Windows 7. Se trata de la versión de Windows Installer que se proporciona con el sistema operativo.
-   Use Windows Installer 4,5 en Windows Server 2008, Windows Server 2003 con Service Pack 1 (SP1), Windows Vista con Service Pack 1 (SP1) o Windows XP con Service Pack 2 (SP2). Para obtener información sobre cómo obtener la última versión de Windows Installer, vea [Windows Installer redistribuibles](windows-installer-redistributables.md).
-   Use Windows Installer 3,1 en Windows 2000 con Service Pack 3 (SP3). Windows Installer versión 3,1 tiene características que facilitan el mantenimiento y la aplicación de [revisiones](patching.md)de aplicaciones.
-   Muchas características importantes se introdujeron con la versión 3,0 y se enumeran en la sección [no compatible con la versión 2,0 de Windows Installer](not-supported-in-windows-installer-version-2-0.md). Los paquetes de instalación y las actualizaciones que se crearon para Windows Installer 2,0 se pueden instalar con Windows Installer 3,0 y versiones posteriores. Los paquetes de revisión que contienen las nuevas tablas utilizadas por Windows Installer 3,0 se pueden aplicar con versiones anteriores de Windows Installer pero sin la funcionalidad de aplicación de revisiones Windows Installer 3,0. También es posible crear revisiones que requieran explícitamente el Windows Installer 3,0 que no se puede aplicar a versiones anteriores de Windows Installer. Si un usuario no puede actualizar la versión del instalador, asegúrese de que la aplicación o actualización será compatible con una actualización futura del Windows Installer.
-   Para obtener una lista de las características Windows Installer no compatibles con versiones anteriores de Windows Installer, consulte [novedades de Windows Installer](what-s-new-in-windows-installer.md).

## <a name="meet-the-windows-logo-certification-requirements"></a>Cumplir los requisitos de certificación del logotipo de Windows.

-   Incluso si no desea enviar su aplicación al programa del logotipo, siga las directrices de certificación del logotipo para que el paquete de Windows Installer sea mejor. Para obtener información general sobre los requisitos del logotipo y vínculos a programas de certificación de logotipo específicos, consulte [requisitos de Windows Installer y logotipo](windows-installer-and-logo-requirements.md).

## <a name="prepare-the-package-for-localization"></a>Preparar el paquete para la localización.

-   Es una buena práctica preparar la localización en el futuro al crear el paquete de instalación original. Puede seguir el procedimiento de localización de paquetes sugerido en [localizar un paquete de Windows Installer](localizing-a-windows-installer-package.md).

## <a name="update-your-windows-installer-development-tools-and-documentation"></a>Actualice la documentación y las herramientas de desarrollo de Windows Installer.

-   Las [herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md) no son redistribuibles y solo se deben usar las versiones de estas herramientas disponibles en Microsoft. Están disponibles en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md) en el kit de desarrollo de software (SDK) de Microsoft Windows.
-   Varios proveedores de software independientes ofrecen herramientas para crear o modificar paquetes Windows Installer. Estas herramientas pueden proporcionar un entorno de creación de paquetes que puede ser más fácil de usar que las herramientas proporcionadas en el SDK de Windows Installer. Puede obtener más información acerca de estas herramientas desde los recursos de información descritos en [otros orígenes de información de Windows Installer](other-sources-of-windows-installer-information.md).
-   La capacidad de crear un paquete a partir de archivos de texto puede ser más intuitiva para algunos desarrolladores. El conjunto de herramientas de Windows Installer XML (WiX) disponible en [sourceforge.net](https://sourceforge.net/projects/wix) crea paquetes de instalación de Windows a partir del código fuente XML.
-   La documentación del [SDK de Windows Installer](./windows-installer-portal.md) Publicada en MSDN Online Library se actualiza con más frecuencia.
-   Use la versión reciente de [Msizap.exe](msizap-exe.md) (versión 3.1.4000.2726 o superior) que está disponible en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md) de Windows Vista o superior. Las versiones inferiores de Msizap.exe pueden quitar información acerca de todas las actualizaciones que se han aplicado a otras aplicaciones en el equipo del usuario. Si se quita esta información, es posible que sea necesario quitar y volver a instalar estas otras aplicaciones para recibir actualizaciones adicionales.
-   El editor de tablas de base de datos [Orca.exe](orca-exe.md) es un editor de tablas de base de datos para crear y editar paquetes de Windows Installer y módulos de combinación. Tiene una interfaz de GUI básica, pero admite la edición avanzada de bases de datos de Windows Installer. Incluso si utiliza otra aplicación como herramienta de desarrollo principal, puede que le resulte más práctico usar Orca.exe para solucionar problemas y probar un paquete.
-   Vea [otras fuentes de información Windows Installer](other-sources-of-windows-installer-information.md) para obtener información sobre Windows Installer actuales disponible en blogs, chats técnicos, grupos de noticias, artículos técnicos y sitios Web.

## <a name="if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices"></a>Si decide volver a empaquetar una aplicación de instalación heredada, siga las prácticas recomendadas para el empaquetado.

Muchos proveedores de aplicaciones proporcionan paquetes de Windows Installer nativa para la instalación o sus productos. El software que convierte una aplicación de instalación heredada existente en un paquete de Windows Installer se denomina herramienta de reempaquetado. La guía paso a paso de las notas del producto sobre la [creación de paquetes de Windows Installer y el reempaquetado del software para la Windows Installer](https://www.microsoft.com/technet/prodtechnol/windows2000serv/howto/winstall.mspx) describe una herramienta de reempaquetado disponible comercialmente. Volver a empaquetar una aplicación de instalación existente no es la mejor práctica de desarrollo. Las aplicaciones que se han diseñado desde el principio para aprovechar las características de Windows Installer pueden ser más fáciles de instalar y de dar servicio a los usuarios. Si decide usar un software de reempaquetado, las siguientes prácticas pueden ayudarle a generar un mejor Windows Installer paquete.

-   Las herramientas de reempaquetado convierten las instalaciones heredadas en un paquete de Windows Installer tomando una imagen de un sistema de almacenamiento provisional antes y después de la instalación. Los cambios en el registro, los cambios de archivo o la configuración del sistema que se produce durante el proceso de captura se incluyen en la instalación de. Configure el hardware y el software del equipo que se usa para volver a empaquetar la instalación lo más cerca posible del sistema del usuario previsto. Cree un paquete independiente para cada configuración de hardware diferente. Volver a empaquetar con un equipo de ensayo limpio. Quite las aplicaciones innecesarias. Detenga todos los procesos innecesarios. Cierre todos los servicios del sistema no esenciales.
-   Realice siempre una copia de la instalación original antes de empezar a trabajar en ella. Trabaje siempre en la copia. Nunca detenga un reempaquetador antes de que termine de compilar el paquete. Si el reempaquetador daña el paquete, seguirá teniendo el original.
-   No volver a empaquetar las actualizaciones de software de Microsoft en un paquete de Windows Installer. Microsoft publica actualizaciones de software, como Service Packs, como archivos de extracción automática que ejecutan la instalación automáticamente. Estas actualizaciones usan instaladores diferentes a los Windows Installer para reemplazar los recursos protegidos de Windows y no se pueden convertir en un paquete de Windows Installer. Para obtener información sobre cómo implementar los Service Pack de Windows, consulte la guía de implementación de Service Pack en [Microsoft TechNet](https://technet.microsoft.com/).
-   No use una herramienta de reempaquetado para convertir un paquete de Windows Installer en un nuevo paquete. El Windows Installer agrega información de configuración al sistema, así como a los recursos de la aplicación. Cuando una herramienta de reempaquetado compara el sistema antes y después de la instalación, el reempaquetador interpreta erróneamente la información de configuración como parte de la aplicación. Normalmente, esto daña la aplicación reempaquetada. En su lugar, use las [transformaciones de personalización](a-customization-transform-example.md) para modificar un paquete de Windows Installer existente o crear un nuevo paquete. Puede crear transformaciones de personalización con la herramienta [Msitran.exe](msitran-exe.md) .
-   No use una herramienta de reempaquetado para consolidar varios paquetes de Windows Installer en un solo paquete. En su lugar, puede usar la herramienta [Msistuff.exe](msistuff-exe.md) para configurar el archivo ejecutable Setup.exe bootstrap para instalar los paquetes uno tras otro.
-   Cree el paquete de Windows Installer para que el cliente pueda personalizarlo fácilmente. Las variables globales utilizadas por el Windows Installer durante una instalación se pueden establecer mediante [propiedades](properties.md) públicas o [transformaciones de personalización](a-customization-transform-example.md). Proporcione documentación para el uso de esas propiedades y valores predeterminados prácticos para todos los valores personalizables. Para obtener información sobre cómo obtener y establecer las propiedades, vea [usar propiedades](using-properties.md). Para obtener un ejemplo de una transformación de personalización, vea [un ejemplo de transformación de personalización](a-customization-transform-example.md).

## <a name="do-not-try-to-replace-protected-resources"></a>No intente reemplazar los recursos protegidos.

Windows Installer paquetes no deben intentar reemplazar los recursos protegidos durante la instalación o actualización. En el Windows Installer no se quitan ni reemplazan estos recursos porque Windows evita la sustitución de archivos esenciales del sistema, carpetas y claves del registro. La protección de estos recursos evita errores en la aplicación y en el sistema operativo.

-   Cuando se ejecuta en Windows Server 2008 o Windows Vista, el Windows Installer omite la instalación de cualquier archivo o clave del registro que esté protegido por [protección de recursos de Windows](../wfp/windows-resource-protection-portal.md) (WRP), el instalador escribe una advertencia en el archivo de registro y continúa con el resto de la instalación sin un error. Para obtener más información, vea [usar Windows Installer y protección de recursos de Windows](windows-resource-protection-on-windows-vista.md).
-   WRP es el nuevo nombre de protección de archivos de Windows (WFP). WRP protege las claves del registro y las carpetas, así como los archivos esenciales del sistema. En Windows Server 2003, Windows XP y Windows 2000, cuando el Windows Installer encontró un archivo protegido con WFP, el instalador solicitaría que WFP instalara el archivo. Para obtener más información, vea [usar Windows Installer y protección de recursos de Windows](windows-resource-protection-on-windows-vista.md).

## <a name="do-not-depend-upon-non-critical-resources"></a>No dependa de recursos no críticos.

La instalación o actualización no debe depender de la instalación de recursos no críticos por los siguientes motivos.

-   Se puede producir un error en las acciones personalizadas si dependen de un componente que pertenece a una característica que el usuario anuncia en lugar de instalarse.
-   Acciones personalizadas secuenciadas antes de que se pueda producir un error en la acción [InstallFinalize](installfinalize-action.md) si dependen de un componente que contiene un ensamblado que se está instalando. El Windows Installer no confirma los ensamblados en la caché de ensamblados global (GAC) hasta que se completa la acción InstallFinalize.

## <a name="use-the-api-to-retrieve-windows-installer-configuration-information"></a>Use la API para recuperar la información de configuración de Windows Installer.

La instalación de la aplicación o actualización no debe depender del acceso directo a Windows Installer información de configuración guardada en el equipo. En su lugar, use la interfaz de programación de aplicaciones de Windows Installer para recuperar la información de configuración. La ubicación y el formato de la información de configuración la administra el servicio de Windows Installer y puede cambiar.

-   Las funciones de instalación y configuración de la API de Windows Installer se describen en la referencia de la [función de instalador](installer-function-reference.md).
-   Las [propiedades de configuración](property-reference.md) se describen en la referencia de propiedad.
-   Los métodos y propiedades de automatización se describen en la referencia de la [interfaz de automatización](automation-interface-reference.md). El script de ejemplo WiLstPrd.vbs se conecta a un objeto de instalador y enumera los productos registrados y la información del producto. Para obtener información, consulte [lista de productos, propiedades, características y componentes](list-products-properties-features-and-components.md).

## <a name="organize-the-installation-of-your-application-around-components"></a>Organice la instalación de la aplicación en torno a los componentes.

El servicio Windows Installer instala o quita colecciones de recursos a los que se hace referencia como [componentes](windows-installer-components.md)de. Dado que los componentes suelen compartirse, el autor de un paquete de instalación debe cumplir las reglas al especificar los componentes de una característica o aplicación.

-   Adhiere a las reglas de componentes al [organizar las aplicaciones en componentes](organizing-applications-into-components.md) para asegurarse de que los nuevos componentes, o nuevas versiones de los componentes, se pueden instalar y quitar sin dañar otras aplicaciones. Puede seguir el procedimiento descrito en [definir los componentes del instalador](defining-installer-components.md).
-   El instalador realiza un seguimiento de todos los componentes por el GUID del identificador de componente correspondiente especificado en la [tabla de componentes](component-table.md). Es esencial para el funcionamiento del mecanismo de recuento de referencias Windows Installer que el GUID del identificador de componente es correcto. Siga las instrucciones que se indican en [cambiar el código de componente](changing-the-component-code.md).
-   Si el paquete debe interrumpir las reglas de componentes, tenga en cuenta las posibles consecuencias y asegúrese de que la instalación nunca instala estos componentes en los que pueden dañar componentes en el sistema del usuario. Para obtener información, consulte [¿Qué ocurre si se interrumpen las reglas de componentes?](what-happens-if-the-component-rules-are-broken.md)
-   Tenga en cuenta cómo el Windows Installer aplica las [reglas de control de versiones de archivo](file-versioning-rules.md) al [reemplazar los archivos existentes](replacing-existing-files.md). El Windows Installer primero determina si el archivo de clave del componente ya está instalado antes de intentar instalar cualquiera de los archivos del componente. Si el instalador encuentra un archivo con el mismo nombre que el archivo de clave del componente instalado en la ubicación de destino, compara la versión, la fecha y el idioma de los dos archivos de clave y utiliza reglas de control de versiones de archivo para determinar si se debe instalar el componente proporcionado por el paquete. Si el instalador determina que debe reemplazar la base del componente en el archivo de clave, utiliza las reglas de control de versiones de archivo en cada archivo instalado para determinar si se debe reemplazar el archivo.

## <a name="reduce-the-size-of-large-windows-installer-packages"></a>Reduzca el tamaño de los paquetes de Windows Installer de gran tamaño.

Los paquetes de Windows muy grandes tienen recursos del sistema y pueden ser difíciles de instalar. Se recomienda reducir el tamaño de los paquetes de Windows Installer muy grandes mediante los métodos siguientes.

-   Comprima los archivos de la instalación y almacénelos en un archivo contenedor (. cab). El instalador permite que el archivo. cab se almacene como un archivo externo independiente o como un flujo de datos en el propio paquete MSI. Para obtener información [, consulte uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).
-   Elimine el espacio de almacenamiento desperdiciado en el archivo. msi mediante una de las opciones descritas en [reducir el tamaño de un archivo. msi](reducing-the-size-of-an--msi-file.md).
-   Si el paquete de Windows Installer contiene más de 32767 archivos, debe cambiar el esquema de la base de datos. Para obtener información, consulte [crear un paquete de gran tamaño](authoring-a-large-package.md).

## <a name="if-you-use-custom-actions-follow-good-custom-action-practices"></a>Si usa acciones personalizadas, siga las prácticas recomendadas para acciones personalizadas.

El Windows Installer tiene muchas [acciones estándar](standard-actions-reference.md) integradas para la instalación y el mantenimiento de aplicaciones. Los desarrolladores deben intentar confiar en las acciones estándar tanto como sea práctico, en lugar de crear sus propias [acciones personalizadas](custom-actions.md). Sin embargo, hay situaciones en las que el desarrollador de un paquete de instalación encuentra que es necesario escribir una acción personalizada.

-   Siga las instrucciones para el [uso de acciones personalizadas](using-custom-actions.md).
-   Siga las [directrices para proteger las acciones personalizadas](guidelines-for-securing-custom-actions.md). Las acciones personalizadas que utilizan información confidencial no deben escribir esta información en el registro. Para obtener información, consulte Seguridad de la [acción personalizada](custom-action-security.md).
-   Las acciones personalizadas no deben intentar establecer un punto de entrada de restauración del sistema desde una acción personalizada. Para obtener información, vea [establecer un punto de restauración desde una acción personalizada](setting-a-restore-point-from-a-custom-action.md).
-   Devuelva los mensajes de error de las acciones personalizadas y escríbalos en el registro para facilitar la solución de problemas de acciones personalizadas. Para obtener información, consulte [acciones personalizadas de mensajes de error](error-message-custom-actions.md) y [devolución de mensajes de error a partir de acciones personalizadas](returning-error-messages-from-custom-actions.md).
-   No cambie el estado del sistema de una acción personalizada inmediata. Las acciones personalizadas que cambian el sistema directamente o que llaman a otro servicio del sistema se deben diferir en el momento en que se ejecuta el script de instalación. Cada [acción personalizada de ejecución aplazada](deferred-execution-custom-actions.md) que cambia el estado del sistema debe ir precedida de una [acción personalizada rollback](rollback-custom-actions.md) para deshacer el cambio de estado del sistema en una reversión de instalación. Para obtener información, consulte [cambiar el estado del sistema mediante una acción personalizada](changing-the-system-state-using-a-custom-action.md).
-   Las acciones personalizadas que realizan operaciones de instalación complejas deben ser un [archivo ejecutable](executable-files.md) o una [biblioteca de vínculos dinámicos](dynamic-link-libraries.md). Limite el uso de acciones personalizadas basadas en [scripts](scripts.md) a operaciones de instalación sencillas.
-   Facilite los detalles de lo que hace la acción personalizada al sistema para que los administradores del sistema puedan detectar fácilmente. Coloque los detalles de las entradas del registro y los archivos usados por la acción personalizada en una tabla personalizada y haga que la acción personalizada se lea desde esta tabla. Esto se muestra en el ejemplo de [uso de una acción personalizada para crear cuentas de usuario en un equipo local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md). Para obtener información sobre cómo agregar tablas personalizadas a una base de datos, vea [trabajar con consultas](working-with-queries.md) y [ejemplos de consultas de base de datos mediante SQL y script](examples-of-database-queries-using-sql-and-script.md).
-   Una acción personalizada no debe mostrar un cuadro de diálogo. Las acciones personalizadas que requieren una interfaz de usuario pueden usar la función [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) en su lugar. Consulte [envío de mensajes a Windows Installer mediante MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).
-   Las acciones personalizadas no deben usar ninguna de las funciones enumeradas en la página: [funciones que no se usan en acciones personalizadas](functions-not-for-use-in-custom-actions.md).
-   Si la instalación está diseñada para ejecutarse en un servidor de Terminal Server, compruebe que todas las acciones personalizadas pueden ejecutarse en un servidor de Terminal Server. Para obtener más información, consulte propiedad [**TerminalServer**](terminalserver.md) .
-   Para que se ejecute una acción personalizada cuando se desinstale una revisión determinada, la acción personalizada debe estar presente en la aplicación original o debe estar en una revisión para el producto que siempre se aplica. Para obtener más información, consulte Revisión de la [desinstalación de acciones personalizadas](patch-uninstall-custom-actions.md).
-   Las acciones personalizadas no deben usar el nivel de interfaz de usuario como condición para enviar mensajes de error al instalador, ya que esto puede interferir con el registro y los mensajes externos. Para obtener información, vea [determinar el nivel de interfaz de usuario desde una acción personalizada](determining-ui-level-from-a-custom-action.md).
-   Use instrucciones condicionales y la sintaxis de la [instrucción condicional](conditional-statement-syntax.md) para asegurarse de que el paquete ejecuta correctamente las acciones personalizadas, no ejecuta acciones personalizadas o ejecuta una acción personalizada alternativa cuando se desinstala el paquete. Compruebe que el paquete funciona según lo previsto al [desinstalar acciones personalizadas](uninstalling-custom-actions.md). Para obtener información, consulte [operaciones de acondicionamiento que se ejecutan durante la eliminación](conditioning-actions-to-run-during-removal.md) .
-   Si la instalación debe ser capaz de ser ejecutada por usuarios que no tienen privilegios de administrador, realice una prueba para asegurarse de que todas las acciones personalizadas se pueden ejecutar con privilegios que no son de administrador. Las acciones personalizadas requieren privilegios elevados para modificar partes del sistema que no son específicas del usuario. El instalador puede ejecutar acciones personalizadas con privilegios elevados si se instala una aplicación administrada o si se ha especificado la Directiva del sistema para privilegios elevados. Todas las acciones personalizadas que requieren privilegios elevados deben incluir la acción personalizada msidbCustomActionTypeInScript y msidbCustomActionTypeNoImpersonate [In-Script las opciones de ejecución](custom-action-in-script-execution-options.md) en el tipo de acción personalizada. Esto se muestra en el ejemplo de [uso de una acción personalizada para crear cuentas de usuario en un equipo local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md).

## <a name="if-you-use-assemblies-follow-good-assembly-practices"></a>Si utiliza ensamblados, siga las prácticas recomendadas para el ensamblado

Si el paquete utiliza [ensamblados](assemblies.md)de software, siga las directrices para [Agregar ensamblados a un paquete](adding-assemblies-to-a-package.md), [Actualizar ensamblados](updating-assemblies.md)e [instalar y quitar ensamblados](installing-and-removing-assemblies.md).

## <a name="do-not-ship-concurrent-installations"></a>No distribuir instalaciones simultáneas.

Las [instalaciones simultáneas](concurrent-installations.md), también denominadas instalaciones anidadas, instalan otro paquete de Windows Installer durante una instalación en ejecución. El uso de instalaciones simultáneas no es una buena práctica porque son difíciles de atender a los clientes. Es posible que la revisión y la actualización no funcionen con instalaciones simultáneas. La alternativa recomendada al uso de instalaciones simultáneas es usar en su lugar una aplicación de instalación y un controlador de interfaz de usuario externo para instalar varios paquetes de Windows Installer de forma secuencial.

Para obtener más información sobre el uso de un controlador de interfaz de usuario externo, vea [supervisar una instalación mediante MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md). Para obtener más información sobre el uso de un controlador externo basado en registros, vea [supervisar una instalación mediante MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).

Las instalaciones simultáneas se utilizan a veces en entornos corporativos controlados para instalar aplicaciones que no están pensadas para el público. Siga estas instrucciones si decide usar instalaciones simultáneas.

-   No use instalaciones simultáneas para instalar o actualizar un producto de envío.
-   Las instalaciones simultáneas no deben compartir componentes.
-   Una instalación administrativa no debe contener una instalación simultánea.
-   Los ProgressBar integrados no deben usarse con instalaciones simultáneas.
-   Los recursos que se van a anunciar no deben instalarse mediante una instalación simultánea.
-   Un paquete que realiza una instalación simultánea de una aplicación también debe desinstalar la aplicación simultánea cuando se desinstale el producto primario. Existe una instalación anidada en el contexto del producto primario en Agregar o quitar programas en el panel de control.

## <a name="keep-package-names-and-package-codes-consistent"></a>Mantener los nombres de paquete y los códigos de paquete coherentes.

El archivo. msi puede tener cualquier nombre que ayude a los usuarios a identificar el paquete, pero el nombre no debe cambiarse sin cambiar también el código de producto.

-   Asigne al archivo. msi un nombre descriptivo que permita al usuario identificar el contenido del paquete de Windows Installer.
-   El [código de producto](product-codes.md) es la identificación principal de una aplicación y debe cambiar siempre que haya una actualización completa de la aplicación. Para obtener más información, vea [**ProductCode**](productcode.md) y [cambiar el código de producto](changing-the-product-code.md). Cambiar el nombre del archivo. msi de la aplicación se considera un cambio completo y siempre requiere un cambio correspondiente del código del producto para mantener la coherencia.
-   El [código del paquete](package-codes.md) es el identificador principal que usa el instalador para buscar y validar el paquete correcto para una instalación determinada. Dos archivos. msi no idénticos deben tener el mismo código de paquete. Si se cambia un paquete sin cambiar el código de paquete, es posible que el instalador no use el paquete más reciente si ambos siguen siendo accesibles para el instalador. El código del paquete se almacena en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) de la secuencia de información de [Resumen](summary-information-stream.md).
-   Tenga en cuenta que las letras del código de producto y los [GUID](guid.md) de código de paquete deben estar en mayúsculas.

## <a name="do-not-use-the-selfreg-and-typelib-tables"></a>No utilice las tablas SelfReg y TypeLib.

-   Se recomienda encarecidamente a los autores de paquetes de instalación que utilicen el registro automático y la tabla [SelfReg](selfreg-table.md) . En su lugar, deben registrar módulos mediante la creación de una o varias tablas en el [Grupo tablas del registro](registry-tables-group.md). Muchas de las ventajas de los Windows Installer se pierden con el registro automático porque las rutinas de registro automático suelen ocultar la información de configuración crítica. Para obtener una lista de las razones para evitar el registro propio, consulte [tabla SelfReg](selfreg-table.md).
-   Se recomienda encarecidamente a los autores de paquetes de instalación que utilicen la tabla [typelib](typelib-table.md) . En lugar de utilizar la tabla TypeLib, registre las bibliotecas de tipos mediante la tabla [del registro](registry-table.md) . Si se produce un error en una instalación con la tabla TypeLib y se debe revertir, es posible que la reversión no restaure el equipo al mismo estado que existía antes de la reversión.

## <a name="provide-the-option-to-install-without-a-user-interface"></a>Proporcione la opción de instalación sin una interfaz de usuario.

A menudo, los administradores prefieren implementar aplicaciones dentro de una empresa sin necesidad de interacción del usuario. Se recomienda habilitar la aplicación para que proporcione la opción de instalar con el [nivel de interfaz de usuario](user-interface-levels.md) ninguno.

-   Use [las propiedades públicas](public-properties.md) para obtener información de configuración. Los administradores pueden proporcionar esta información en la línea de comandos.
-   No es necesario que la instalación dependa de la información recopilada de la interacción del usuario con los cuadros de diálogo. Esta información no está disponible durante una instalación silenciosa.
-   No reinicie automáticamente el equipo del usuario durante una instalación silenciosa.
-   Los administradores pueden establecer el [nivel](user-interface-levels.md) de la interfaz de usuario al instalar mediante la [opción de línea de comandos](command-line-options.md) "/q". El nivel de interfaz de usuario también se puede establecer mediante programación con una llamada a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).

## <a name="avoid-using-the-alwaysinstallelevated-policy"></a>Evite el uso de la Directiva AlwaysInstallElevated.

Si no se establece la directiva [AlwaysInstallElevated](alwaysinstallelevated.md) , las aplicaciones no distribuidas por el administrador se instalan con los privilegios del usuario y solo las aplicaciones administradas obtienen privilegios elevados. La configuración de esta directiva indica a Windows Installer que use permisos del sistema cuando instale la aplicación en el sistema. Este método puede abrir un equipo a un riesgo de seguridad, porque cuando se establece esta Directiva, un usuario que no es administrador puede ejecutar instalaciones con privilegios [*elevados*](e-gly.md) y tener acceso a ubicaciones seguras en el equipo. Es aconsejable usar otro método que la Directiva AlwaysInstallElevated al [instalar un paquete con privilegios elevados para una aplicación administrada que no sea de administración o de](installing-a-package-with-elevated-privileges-for-a-non-admin.md) [revisión Per-User](patching-per-user-managed-applications.md).

## <a name="enable-the-disablemedia-policy-to-limit-unauthorized-installation"></a>Habilite la Directiva DisableMedia para limitar la instalación no autorizada.

La directiva [DisableMedia](disablemedia.md) puede impedir la instalación no autorizada de aplicaciones. Cuando esta directiva está habilitada, los usuarios y administradores que ejecuten una instalación de mantenimiento de un producto no podrán usar el cuadro de diálogo examinar para buscar orígenes multimedia, como un CD-ROM, para los orígenes de otros productos instalables. La exploración de otros productos se evita independientemente de si la instalación se realiza con privilegios elevados. Todavía es posible que el usuario vuelva a instalar el producto desde el medio si el usuario tiene un origen de medios correctamente etiquetado.

## <a name="keep-the-original-package-source-files-secure-and-available-to-users"></a>Mantenga los archivos de origen del paquete original seguros y disponibles para los usuarios.

En algunos casos, es posible que se necesite el origen original del paquete de Windows Installer para instalarlo a petición, reparar o actualizar una aplicación. Si el instalador no puede encontrar un origen disponible, se pide al usuario que proporcione medios o que vaya a una ubicación de red que contenga los orígenes necesarios. Se recomienda asegurarse de que el instalador tenga los orígenes que necesita sin tener que preguntar al usuario.

-   Use las [firmas digitales y los archivos. cab externos](digital-signatures-and-external-cabinet-files.md) para asegurarse de que los orígenes origs que usa el instalador son seguros. Una imagen de origen sin comprimir almacenada en una ubicación pública no es segura.
-   Incluya una lista completa de las rutas de acceso de origen de la red o dirección URL al paquete de instalación de la aplicación en la propiedad [**SourceList**](sourcelist.md) .
-   Use un recurso compartido de Sistema de archivos distribuido (DFS) para la ruta de acceso de origen.
-   Use la API de Windows Installer para recuperar y modificar la información de la lista de código fuente para las aplicaciones y revisiones de Windows Installer. Para obtener información, consulte [Administración de orígenes de instalación](managing-installation-sources.md).
-   Use los métodos y las propiedades del [**objeto instalador**](installer-object.md), el [**objeto Product**](product-object.md)y el [**objeto patch**](patch-object.md) para recuperar y modificar la información de la lista de origen de Windows Installer Aplicaciones y revisiones.
-   Adhiere a los puntos que se muestran en [impedir que una revisión requiera acceso a los puntos de origen de la instalación original](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md) para minimizar la posibilidad de que la revisión requiera acceso a los orígenes originales.
-   Almacene los archivos de origen del paquete en una ubicación que no sea la carpeta temporal del sistema. Windows Installer archivos de origen almacenados en la carpeta temporal pueden dejar de estar disponibles para los usuarios.

## <a name="enable-verbose-logging-on-users-computer-when-troubleshooting-deployment"></a>Habilite el registro detallado en el equipo del usuario al solucionar problemas de implementación.

El [registro de Windows Installer](windows-installer-logging.md) incluye una opción de registro detallado que se puede habilitar en el equipo de un usuario. La información de un registro detallado puede resultar útil al intentar solucionar problemas de la implementación del paquete Windows Installer.

-   Puede habilitar el registro detallado en el equipo del usuario mediante [las opciones](command-line-options.md)de la línea de comandos, la propiedad [**MsiLogging**](msilogging.md) , la [Directiva de registro](logging.md), [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)y el método [**EnableLog**](installer-enablelog.md) .
-   Se [Wilogutl.exe](wilogutl-exe.md)un recurso muy útil para interpretar Windows Installer archivos de registro. Esta herramienta ayuda a analizar los archivos de registro y muestra soluciones sugeridas a los errores que se encuentran en un archivo de registro.
-   Para obtener más información acerca de cómo interpretar Windows Installer archivos de registro, vea las notas del producto disponibles en el sitio de TechNet: [Windows Installer: Benefits and Implementation for System Administrators](https://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/winmsi.mspx).
-   La opción de registro detallado solo debe usarse para solucionar problemas y no debe dejarse activada porque puede tener efectos negativos en el rendimiento del sistema y en el espacio en disco. Cada vez que se usa la herramienta Agregar o quitar programas del panel de control, se crea un nuevo archivo.

## <a name="uninstallation-leaves-the-users-computer-in-a-clean-state"></a>La desinstalación deja el equipo del usuario en un estado limpio.

La eliminación de la aplicación es tan importante como la instalación. Cuando se desinstala un paquete de Windows Installer, no debe dejar ninguna parte inútil en el equipo del usuario.

-   Si un archivo que se debería haber quitado del equipo del usuario permanece instalado después de ejecutar una desinstalación, es posible que el instalador no esté quitando el componente que contiene el archivo por una o varias de las razones descritas en [quitar archivos en desuso](removing-stranded-files.md).
-   Si se debe registrar una aplicación, cree el paquete para quitar la información del registro cuando se desinstale la aplicación. Para obtener información, consulte [Agregar o quitar claves del registro en la instalación o eliminación de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). Si una aplicación no está registrada, la aplicación no aparece en la característica agregar o quitar programas del panel de control y no se puede administrar mediante el Windows Installer.
-   Para ocultar una aplicación de la característica agregar o quitar programas del panel de control y seguir pudiendo usar el Windows Installer para administrar la aplicación, siga las instrucciones descritas en [Agregar y quitar una aplicación y no dejar ningún seguimiento en el registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).
-   Las acciones personalizadas deben estar condicionadas a ejecutarse o no según sea necesario durante la desinstalación. Es posible que sea necesario ejecutar diferentes acciones personalizadas al instalar y desinstalar.
-   La información de personalización específica del usuario se puede almacenar en un archivo de texto en el equipo. Esto tiene la ventaja de que el archivo se puede quitar cuando se desinstala la aplicación, incluso si el usuario de esta personalización no ha iniciado sesión actualmente.

## <a name="test-packages-for-both-per-user-and-per-machine-installation-deployment"></a>Probar paquetes para la implementación de instalación por usuario y por equipo.

Se recomienda que los clientes decidan si implementar un paquete para instalarlo en el [contexto de instalación](installation-context.md)por equipo o por usuario.

-   Tenga en cuenta si la aplicación debe estar disponible solo para determinados usuarios o para todos los usuarios del equipo durante el proceso de desarrollo.
-   Compruebe que el paquete funciona correctamente para los contextos de instalación por usuario y por equipo.
-   Facilite la personalización del paquete y permita a los clientes decidir si implementarlos por usuario o por equipo.

## <a name="plan-and-test-a-servicing-strategy-before-shipping-the-application"></a>Planee y pruebe una estrategia de servicio antes de enviar la aplicación.

Debe decidir cómo desea dar servicio a la aplicación antes de implementar la aplicación por primera vez.

-   Tenga en cuenta los tipos de actualizaciones que espera usar para atender su aplicación en el futuro. El Windows Installer proporciona tres tipos de actualizaciones: [Small Update, Small](small-updates.md) [upgrade](minor-upgrades.md)y [major upgrades](major-upgrades.md). Las diferencias entre estos se describen en el tema [revisiones y actualizaciones](patching-and-upgrades.md) .
-   Antes de enviar la aplicación, compruebe que funciona según lo esperado después de dar servicio a cada tipo de actualización.

## <a name="reduce-the-dependency-of-updates-upon-the-original-sources"></a>Reduzca la dependencia de las actualizaciones en los orígenes originales.

Si los archivos de origen originales son necesarios para actualizar la aplicación, esto puede dificultar el mantenimiento de la aplicación. Los métodos siguientes pueden ayudar a reducir la dependencia de las actualizaciones en los orígenes originales.

-   Use una [*revisión diferencial*](d-gly.md) para actualizar las versiones de línea base de la aplicación, como la versión RTM y las versiones Service Pack. Siga las instrucciones para usar las revisiones Delta descritas en el tema: [reducir el tamaño](reducing-patch-size.md)de la revisión.
-   Siga las recomendaciones que se indican en el tema: [impedir que una revisión requiera acceso al origen de la instalación original](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

## <a name="do-not-distribute-unserviceable-merge-modules"></a>No distribuya módulos de combinación no redistribuibles.

Las aplicaciones no deben depender de [módulos de combinación](merge-modules.md) para la instalación de componentes si el propietario del módulo de combinación y el propietario de la aplicación son diferentes. Esto puede dificultar el servicio de la aplicación porque ambos propietarios deben coordinar para actualizar la aplicación o el módulo. Sin conocer todas las aplicaciones que han usado el módulo de combinación, el propietario de la aplicación no puede actualizar el módulo de fusión mediante combinación sin que el riesgo de que la actualización sea incompatible con otra aplicación. El propietario del módulo de combinación no tiene ningún método directo para actualizar Windows Installer paquetes que ya han instalado el módulo de combinación.

-   Considere la posibilidad de proporcionar los componentes necesarios a los usuarios como otro Windows Installer instalación.

## <a name="avoid-patching-administrative-installations"></a>Evite aplicar revisiones a las instalaciones administrativas.

Proporcionar en una red una [instalación administrativa](administrative-installation.md) del paquete de Windows Installer original de la aplicación para permitir a los miembros de un grupo de trabajo instalar la aplicación. Los usuarios de esta imagen administrativa deben aplicar las actualizaciones a la instancia local de la aplicación que se encuentra en su equipo. Esto impide que los usuarios se sincronizan con la imagen administrativa. No se recomienda aplicar actualizaciones a la instalación administrativa por los siguientes motivos.

-   Se incrementa el tamaño y la latencia de la descarga necesaria para que los usuarios obtengan una actualización en comparación con la descarga de una revisión. Todos los archivos de código fuente y paquete de Windows Installer actualizados deben descargar, volver a almacenar en caché y reinstalar.
-   Los usuarios no pueden [instalar](installation-on-demand.md) las aplicaciones a petición y reparar desde una instalación administrativa actualizada hasta que vuelvan a almacenar en caché y reinstalen la aplicación.
-   Al aplicar una revisión a una instalación administrativa, se quita la firma digital del paquete. Un administrador debe volver a firmar el paquete. Para obtener más información sobre el uso de firmas digitales, vea [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md).
-   Muchas revisiones binarias tienen como destino la imagen RTM de la aplicación y requieren una versión anterior del archivo. Es posible que la instancia local de una aplicación instalada desde una instalación administrativa actualizada no funcione con otras actualizaciones. Muchas aplicaciones de revisión binaria pueden producir errores.
-   Al aplicar una revisión a una instalación administrativa, se actualizan los archivos de origen y el archivo. msi, pero no se marca la imagen de red con información sobre la actualización. Los usuarios no pueden determinar qué actualizaciones han recibido de la instalación administrativa. Esto hace que sea imposible secuenciar las actualizaciones aplicadas en el lado del usuario con las que ya se han aplicado en el lado de la imagen administrativa.
-   Las revisiones aplicadas a una instalación administrativa no son revisiones que no se pueden [instalar](uninstallable-patches.md). Esto puede impedir que el código de paquete almacenado en caché en el equipo del usuario sea diferente del código del paquete en la instalación administrativa. Si el código de paquete almacenado en memoria caché en el equipo del usuario se diferencia de los de la instalación administrativa, vuelva a instalar la aplicación desde la instalación administrativa y, a continuación, aplique una revisión al equipo cliente.
-   Si decide aplicar actualizaciones pequeñas mediante la aplicación de revisiones en una imagen administrativa, siga las directrices descritas en el tema: [aplicar actualizaciones pequeñas mediante la aplicación de revisiones en una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md).

## <a name="register-updates-to-run-with-elevated-privilege"></a>Registra las actualizaciones para que se ejecuten con privilegios elevados.

A partir de Windows Installer 3,0, es posible aplicar revisiones a una aplicación que se ha instalado en un contexto administrado por el usuario, una vez que se ha registrado la revisión como con privilegios elevados. No se pueden aplicar revisiones a las aplicaciones que se instalan en un contexto administrado por usuario con versiones de Windows Installer anteriores a la versión 3,0.

-   Use el método [**SourceListAddSource**](patch-sourcelistaddsource.md) o la función [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para registrar un paquete de revisión como con privilegios elevados. Siga las instrucciones y los ejemplos proporcionados en la [aplicación de revisiones Per-User aplicaciones administradas](patching-per-user-managed-applications.md).
-   Al ejecutar Windows Installer versión 4,0 en Windows Vista, también puede usar la aplicación de [revisiones del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md) para permitir a los autores de instalaciones de Windows Installer identificar revisiones firmadas digitalmente que los usuarios que no son administradores pueden aplicar en el futuro. Esto solo está disponible con la instalación de paquetes en el [contexto de instalación](installation-context.md) por máquina (ALLUSERS = 1).
-   Asegúrese de que la revisión con privilegios mínimos no se ha deshabilitado mediante el establecimiento de la propiedad [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) o de la directiva [DisableLUAPatching](disableluapatching.md) .

## <a name="use-the-msipatchsequence-table-to-sequence-patches"></a>Use la tabla MsiPatchSequence para secuenciar las revisiones.

Incluya una [tabla MsiPatchSequence](msipatchsequence-table.md) en el paquete y agregue la información de secuenciación de revisiones. A partir de Windows Installer versión 3,0, el instalador puede usar la tabla MsiPatchSequence al [instalar varias revisiones](installing-multiple-patches.md) para determinar la mejor secuencia de aplicación de revisiones. Siga las instrucciones que se describen en las notas del producto de la [secuencia de revisión en Windows Installer versión 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3) para definir familias de revisiones.

-   Si es práctico, especifique todas las revisiones como pertenecientes a una única familia de revisiones. En muchos casos, una sola familia de revisiones proporciona la flexibilidad suficiente para la secuencia de revisiones. La complejidad de la creación aumenta cuando se usan varias familias de revisiones. Asigne un nombre descriptivo a la familia de revisiones y asigne valores de secuencia en esa familia de revisiones que aumenten con el tiempo. Siga el ejemplo de aplicación de [revisiones múltiple](multiple-patching-example.md) para aplicar revisiones en el orden en que se han emitido.
-   Use la [tabla PatchSequence](patchsequence-table--patchwiz-dll-.md) de la [Patchwiz.dll](patchwiz-dll.md) para generar la información en la [tabla MsiPatchSequence](msipatchsequence-table.md). La versión de PATCHWIZ.DLL que se lanzó con Windows Installer 3,0 puede generar automáticamente información de secuenciación de revisiones. Para obtener más información sobre cómo agregar una nueva revisión, vea [generar información de secuencia de revisión](generating-patch-sequence-information---patchwiz-dll-.md). Para obtener más información sobre los escenarios de secuenciación de revisiones, vea las notas del producto: [secuencia de revisiones en Windows Installer versión 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3).

## <a name="test-the-installation-package-thoroughly"></a>Pruebe el paquete de instalación exhaustivamente.

Compruebe si la instalación, la reparación y la eliminación del paquete de Windows Installer son correctas. Puede dividir el proceso de prueba en las siguientes partes.

-   Pruebas de instalación: Pruebe la instalación con todas las posibles combinaciones de características de la aplicación. Probar todos los tipos de instalación, incluida la instalación [administrativa](administrative-installation.md), la [instalación de reversión](rollback-installation.md)y [la instalación a petición](installation-on-demand.md). Pruebe todos los posibles métodos de instalación, como hacer clic en el archivo. msi, opciones de la [línea de comandos](command-line-options.md)e instalar desde el panel de control. Compruebe que los usuarios pueden instalar el paquete en todos los contextos de privilegios posibles. Intente instalar el paquete después de haber sido implementado por todos los métodos posibles. Habilite el [registro de Windows Installer](windows-installer-logging.md) para cada prueba y resuelva todos los errores que se encuentren en el registro del instalador y en el registro de eventos.
-   Pruebas de interfaz de usuario: prueba el paquete cuando se instala con todos los [niveles de interfaz de usuario](user-interface-levels.md)posibles. Pruebe el paquete instalado sin interfaz de usuario y con toda la información proporcionada a través de la interfaz de usuario. Asegúrese de que la interfaz de usuario tiene [accesibilidad](accessibility.md) y que la interfaz de usuario funciona según lo esperado para las diferentes resoluciones de pantalla y tamaños de fuente.
-   Pruebas de mantenimiento y reparación: Compruebe que el paquete puede controlar la [revisión y las actualizaciones](patching-and-upgrades.md) entregadas por una [actualización pequeña](small-updates.md), una [actualización mínima](minor-upgrades.md)y [actualizaciones importantes](major-upgrades.md). Antes de implementar el paquete, escriba una actualización de prueba de cada tipo e intente aplicarla al paquete original.
-   Desinstalar pruebas: Compruebe que cuando se quita el paquete no deja ninguna parte no útil en el equipo del usuario y que solo se ha quitado la información que pertenece al paquete. Reinicie el equipo de pruebas después de desinstalar el paquete y comprobar la integridad de las herramientas comunes del sistema y otras aplicaciones estándar. Compruebe que los usuarios pueden quitar el paquete en todos los contextos de privilegios posibles. Probar todos los métodos para quitar el paquete, haga clic en el archivo. msi, pruebe con las opciones de la [línea de comandos](command-line-options.md)y pruebe a quitar el paquete del panel de control. Habilite el [registro de Windows Installer](windows-installer-logging.md) para cada prueba y resuelva todos los errores que se encuentren en el registro del instalador y en el registro de eventos.
-   Pruebas de funcionalidad del producto: Asegúrese de que la aplicación funciona según lo esperado después de la instalación, reparación o eliminación del paquete.

## <a name="fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package"></a>Corrija todos los errores de validación antes de implementar un paquete de instalación nuevo o revisado.

Ejecute la [validación de paquetes](package-validation.md) en un paquete de Windows Installer nuevo o revisado antes de intentar instalarlo por primera vez. La validación comprueba la base de datos de Windows Installer para los errores de creación. Si intenta instalar un paquete que no supera la validación, puede dañar el sistema del usuario.

-   Puede validar el paquete mediante [Orca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md). Las dos herramientas se proporcionan con el Windows SDK. Los proveedores de terceros también pueden incorporar el sistema de validación de ICE en su entorno de creación.
-   Puede usar el conjunto estándar de [evaluadores de coherencia interna (CIEM)](internal-consistency-evaluators-ices.md) incluido en los archivos. Cub proporcionados con el SDK o personalizar la validación mediante la [creación de un ICE](building-an-ice.md) y su adición al archivo. Cub.
-   Puede utilizar la Evalcom2.dll para implementar la [automatización](validation-automation.md) de la validación para los paquetes de instalación y los módulos de combinación.

## <a name="author-a-secure-installation"></a>Cree una instalación segura.

Siga estas instrucciones al desarrollar el paquete para ayudar a mantener un entorno seguro durante la instalación.

-   [Directrices para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md)
-   [Directrices para proteger paquetes en equipos bloqueados](guidelines-for-securing-packages-on-locked-down-computers.md)
-   [Directrices para proteger las acciones personalizadas](guidelines-for-securing-custom-actions.md)

## <a name="use-pmsihandle-instead-of-handle"></a>Usar PMSIHANDLE en lugar de HANDLE

Las variables de tipo **PMSIHANDLE** se definen en MSI. h. Se recomienda que la aplicación use el tipo **PMSIHANDLE** porque el instalador cierra los objetos **PMSIHANDLE** cuando salen del ámbito, mientras que la aplicación debe cerrar los objetos **MSIHANDLE** llamando a [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).

Por ejemplo, si utiliza código similar al siguiente:

``` syntax
MSIHANDLE hRec = MsiCreateRecord(3);
```

Cámbielo a:

``` syntax
PMSIHANDLE hRec = MsiCreateRecord(3);
```

 

 
