---
description: 'En esta sección se enumera una lista de sugerencias, vinculadas a la documentación principal del SDK del instalador de Windows, para ayudar a los desarrolladores de aplicaciones, los autores de la configuración, los profesionales de TI y los desarrolladores de infraestructura a descubrir los procedimientos recomendados para usar el instalador de Windows:'
ms.assetid: ff48d995-fe6f-4d1b-898d-67574ed3c5b7
title: Windows Procedimientos recomendados del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffaf6aae83afbe510f2b1eefc447e34754296ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069577"
---
# <a name="windows-installer-best-practices"></a>Windows Procedimientos recomendados del instalador

En esta sección se enumera una lista de sugerencias, vinculadas a la documentación principal del SDK del instalador de Windows, para ayudar a los desarrolladores de aplicaciones, los autores de la configuración, los profesionales de TI y los desarrolladores de infraestructura a descubrir los procedimientos recomendados para usar el instalador de Windows:

-   [Actualice la versión Windows instalador.](#update-the-windows-installer-version)
-   [Cumpla los requisitos Windows certificación del logotipo del usuario.](#meet-the-windows-logo-certification-requirements)
-   [Prepare el paquete para la localización.](#prepare-the-package-for-localization)
-   [Actualice la documentación y las herramientas de desarrollo del instalador de Windows.](#update-your-windows-installer-development-tools-and-documentation)
-   [Si decide volver a empaquetar una aplicación de configuración heredada, siga las prácticas de reempaquetado adecuadas.](#if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices)
-   [No intente reemplazar los recursos protegidos.](#do-not-try-to-replace-protected-resources)
-   [No dependa de recursos no críticos.](#do-not-depend-upon-non-critical-resources)
-   [Use la API para recuperar Windows configuración del instalador.](#use-the-api-to-retrieve-windows-installer-configuration-information)
-   [Organice la instalación de la aplicación en torno a los componentes.](#organize-the-installation-of-your-application-around-components)
-   [Reduzca el tamaño de los paquetes Windows Installer.](#reduce-the-size-of-large-windows-installer-packages)
-   [Si usa acciones personalizadas, siga los procedimientos de acción personalizados recomendados.](#if-you-use-custom-actions-follow-good-custom-action-practices)
-   [Si usa ensamblados, siga los procedimientos recomendados de ensamblado.](#if-you-use-assemblies-follow-good-assembly-practices)
-   [No envíe instalaciones simultáneas.](#do-not-ship-concurrent-installations)
-   [Mantener coherentes los nombres de paquetes y los códigos de paquete.](#keep-package-names-and-package-codes-consistent)
-   [No use las tablas SelfReg y TypeLib.](#do-not-use-the-selfreg-and-typelib-tables)
-   [Proporcione la opción para instalar sin una interfaz de usuario.](#provide-the-option-to-install-without-a-user-interface)
-   [Evite usar la directiva AlwaysInstallElevated.](#avoid-using-the-alwaysinstallelevated-policy)
-   [Habilite la directiva DisableMedia para limitar la instalación no autorizada.](#enable-the-disablemedia-policy-to-limit-unauthorized-installation)
-   [Mantenga los archivos de origen del paquete original seguros y disponibles para los usuarios.](#keep-the-original-package-source-files-secure-and-available-to-users)
-   [Habilite el registro detallado en el equipo del usuario al solucionar problemas de implementación.](#enable-verbose-logging-on-users-computer-when-troubleshooting-deployment)
-   [La desinstalación deja el equipo del usuario en un estado limpio.](#uninstallation-leaves-the-users-computer-in-a-clean-state)
-   [Pruebe los paquetes para la implementación de instalación por usuario y por máquina.](#test-packages-for-both-per-user-and-per-machine-installation-deployment)
-   [Planee y pruebe una estrategia de mantenimiento antes de enviar la aplicación.](#plan-and-test-a-servicing-strategy-before-shipping-the-application)
-   [Reduzca la dependencia de las actualizaciones en los orígenes originales.](#reduce-the-dependency-of-updates-upon-the-original-sources)
-   [No distribuya módulos de combinación que no son de servicio.](#do-not-distribute-unserviceable-merge-modules)
-   [Evite aplicar revisiones a las instalaciones administrativas.](#avoid-patching-administrative-installations)
-   [Registre las actualizaciones para que se ejecuten con privilegios elevados.](#register-updates-to-run-with-elevated-privilege)
-   [Use la tabla MsiPatchSequence para secuenciar revisiones.](#use-the-msipatchsequence-table-to-sequence-patches)
-   [Pruebe el paquete de instalación exhaustivamente.](#test-the-installation-package-thoroughly)
-   [Corrija todos los errores de validación antes de implementar un paquete de instalación nuevo o revisado.](#fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package)
-   [Cree una instalación segura.](#author-a-secure-installation)
-   [Usar PMSIHANDLE en lugar de HANDLE](#use-pmsihandle-instead-of-handle)

## <a name="update-the-windows-installer-version"></a>Actualice la versión Windows instalador.

-   Use Windows Installer 5.0 en Windows Server 2008 R2 y Windows 7. Esta es la versión Windows installer proporcionada con el sistema operativo.
-   Use Windows Installer 4.5 en Windows Server 2008, Windows Server 2003 con Service Pack 1 (SP1), Windows Vista con Service Pack 1 (SP1) o Windows XP con Service Pack 2 (SP2). Para obtener información sobre cómo obtener la versión más Windows installer, [vea Windows Installer Redistributables](windows-installer-redistributables.md).
-   Use Windows Installer 3.1 en Windows 2000 con Service Pack 3 (SP3). Windows La versión 3.1 del instalador tiene características que facilitan un mejor mantenimiento de las aplicaciones y la [aplicación de revisiones.](patching.md)
-   Muchas características importantes se introdujeron con la versión 3.0 y se enumeran en la sección No se admite en [Windows Installer versión 2.0](not-supported-in-windows-installer-version-2-0.md). Los paquetes de instalación y las actualizaciones que se crearon para Windows Installer 2.0 se pueden instalar mediante Windows Installer 3.0 y versiones posteriores. Los paquetes de revisión que contienen las nuevas tablas usadas por Windows Installer 3.0 todavía se pueden aplicar con versiones anteriores de Windows Installer, pero sin la funcionalidad de aplicación de revisiones de Windows Installer 3.0. También es posible crear revisiones que requieran explícitamente Windows Installer 3.0 que no se pueden aplicar en versiones anteriores de Windows Installer. Si un usuario no puede actualizar la versión del instalador, asegúrese de que la aplicación o actualización sea compatible con una actualización futura del instalador de Windows.
-   Para obtener una lista de las características de Windows Installer no admitidas por versiones anteriores del instalador de Windows, vea Novedades de [Windows Installer](what-s-new-in-windows-installer.md).

## <a name="meet-the-windows-logo-certification-requirements"></a>Cumpla los requisitos Windows certificación del logotipo del usuario.

-   Incluso si no piensa enviar la aplicación al programa de logotipos, seguir las directrices de certificación del logotipo puede ayudar a mejorar Windows Installer. Para obtener información general sobre los requisitos del logotipo y vínculos a programas específicos de certificación de logotipos, consulte Windows [Installer and Logo Requirements](windows-installer-and-logo-requirements.md).

## <a name="prepare-the-package-for-localization"></a>Prepare el paquete para la localización.

-   Es un procedimiento recomendado prepararse para la localización futura al crear el paquete de instalación original. Puede seguir el procedimiento de localización de paquetes sugerido en [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).

## <a name="update-your-windows-installer-development-tools-and-documentation"></a>Actualice la documentación y las herramientas de desarrollo del instalador de Windows.

-   Las [Windows de desarrollo del](windows-installer-development-tools.md) instalador no son redistribuibles y solo debe usar las versiones de estas herramientas disponibles en Microsoft. Están disponibles en los componentes del [SDK Windows para desarrolladores](platform-sdk-components-for-windows-installer-developers.md) Windows Installer en el Kit de desarrollo de software (SDK) de Microsoft Windows.
-   Varios proveedores de software independientes ofrecen herramientas para crear o modificar Windows paquetes del instalador. Estas herramientas pueden proporcionar un entorno de creación de paquetes que puede ser más fácil de usar que las herramientas proporcionadas en el SDK Windows Installer. Puede obtener más información sobre estas herramientas en los recursos de información que se deban a otros orígenes [de Windows información del instalador](other-sources-of-windows-installer-information.md).
-   La funcionalidad de compilar un paquete a partir de archivos de texto puede ser más intuitiva para algunos desarrolladores. El conjunto Windows herramientas XML del instalador [](https://sourceforge.net/projects/wix) de Sourceforge.net (WiX) disponible en Windows paquetes de instalación a partir del código fuente XML.
-   La documentación del [SDK Windows Installer](./windows-installer-portal.md) publicado en MSDN Online Library se actualiza con más frecuencia.
-   Use la versión reciente de [Msizap.exe](msizap-exe.md) (versión 3.1.4000.2726 o posterior) que está disponible en los componentes del SDK de Windows para desarrolladores del instalador de [Windows](platform-sdk-components-for-windows-installer-developers.md) para Windows Vista o posterior. Las versiones inferiores Msizap.exe pueden quitar información sobre todas las actualizaciones que se han aplicado a otras aplicaciones en el equipo del usuario. Si se quita esta información, es posible que estas otras aplicaciones deban quitarse y reinstalarse para recibir actualizaciones adicionales.
-   El editor de tablas de [baseOrca.exe](orca-exe.md) es un editor de tablas de base de datos para crear y editar Windows paquetes del instalador y módulos de combinación. Tiene una interfaz gráfica de usuario básica, pero admite la edición avanzada de bases de Windows installer. Incluso si usa otra aplicación como herramienta de desarrollo principal, es posible que el uso de Orca.exe sea conveniente al solucionar problemas y probar un paquete.
-   Consulte Otros orígenes de [información del](other-sources-of-windows-installer-information.md) instalador de Windows para obtener la información actual del instalador de Windows disponible en blogs, chats técnicos, grupos de noticias, artículos técnicos y sitios web.

## <a name="if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices"></a>Si decide volver a empaquetar una aplicación de configuración heredada, siga las prácticas de reempaquetado adecuadas.

Muchos proveedores de aplicaciones proporcionan paquetes Windows Installer nativos para la instalación o sus productos. El software que convierte una aplicación de instalación heredada existente en un paquete Windows Installer se conoce como una herramienta de reempaquetar. En la guía paso a paso de las instrucciones para crear paquetes del instalador de Windows y volver a empaquetar software para el instalador de [Windows](https://www.microsoft.com/technet/prodtechnol/windows2000serv/howto/winstall.mspx) se describe una herramienta de reempaquetar disponible comercialmente. Volver a empaquetar una aplicación de instalación existente no es el procedimiento de desarrollo recomendado. Las aplicaciones que se han diseñado desde el principio para aprovechar las características de Windows Installer pueden ser más fáciles de instalar y dar servicio a los usuarios. Si decide usar un software de reempaquetar, los procedimientos siguientes pueden ayudarle a generar un mejor Windows instalador.

-   Las herramientas de reempaquetar convierten las instalaciones heredadas en un paquete Windows Installer tomando una imagen de un sistema de ensayo antes y después de la instalación. Los cambios en el Registro, los cambios en los archivos o la configuración del sistema que se producen durante el proceso de captura se incluyen en la instalación. Configure el hardware y el software del equipo que se usa para volver a empaquetar la instalación lo más cerca posible del sistema del usuario previsto. Cree un paquete independiente para cada configuración de hardware diferente. Vuelva a empaquetar con un equipo de ensayo limpio. Quite las aplicaciones innecesarias. Detenga todos los procesos innecesarios. Cierre todos los servicios del sistema no esenciales.
-   Realice siempre una copia de la instalación original antes de empezar a trabajar en ella. Trabaje siempre en la copia. No detenga nunca un reempaquetado antes de que termine de compilar el paquete. Si el reempaquetado daña el paquete, seguirá teniendo el original.
-   No vuelva a empaquetar las actualizaciones de software de Microsoft en un paquete Windows Installer. Microsoft publica actualizaciones de software, como Service Pack, como archivos autoextrayendo que ejecuta automáticamente la instalación. Estas actualizaciones usan instaladores diferentes de Windows Installer para reemplazar los recursos Windows protegidos y no se pueden convertir en un paquete Windows Installer. Para obtener información sobre cómo implementar Windows Service Pack, consulte la guía de implementación del Service Pack en [Microsoft TechNet.](https://technet.microsoft.com/)
-   No use una herramienta de reempaquetar para convertir un paquete Windows Installer en un nuevo paquete. El Windows agrega información de configuración al sistema, así como a los recursos de la aplicación. Cuando una herramienta de reempaquetado compara el sistema antes y después de la instalación, el reempaquetado interpreta erróneamente la información de configuración como parte de la aplicación. Esto suele dañar la aplicación reempaquetado. En su [lugar, use transformaciones de](a-customization-transform-example.md) personalización para modificar un paquete Windows Installer existente o crear un nuevo paquete. Puede crear transformaciones de personalización mediante [ laMsitran.exe](msitran-exe.md) personalizada.
-   No use una herramienta de reempaquetar para consolidar varios paquetes Windows Installer en un único paquete. En su lugar, puede usar [Msistuff.exe](msistuff-exe.md) herramienta para configurar el ejecutable de arranque Setup.exe para instalar los paquetes uno tras otro.
-   Cree el Windows Installer para que el cliente pueda personalizarlo fácilmente. Las variables globales usadas por Windows Installer durante una instalación se pueden establecer mediante propiedades [públicas](properties.md) o transformaciones [de personalización](a-customization-transform-example.md). Proporcione documentación sobre el uso de esas propiedades y los valores predeterminados prácticos para todos los valores personalizables. Para obtener información sobre cómo obtener y establecer propiedades, vea [Using Properties](using-properties.md). Para obtener un ejemplo de una transformación de personalización, vea [Ejemplo de transformación de personalización](a-customization-transform-example.md).

## <a name="do-not-try-to-replace-protected-resources"></a>No intente reemplazar los recursos protegidos.

Windows Los paquetes del instalador no deben intentar reemplazar los recursos protegidos durante la instalación o actualización. El Windows no quita ni reemplaza estos recursos porque Windows impide el reemplazo de archivos, carpetas y claves del Registro esenciales del sistema. La protección de estos recursos evita errores en la aplicación y el sistema operativo.

-   Cuando se ejecuta en Windows Server 2008 o Windows Vista, el instalador de Windows omite la instalación de cualquier archivo o clave del Registro protegido por [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) (WRP), el instalador escribe una advertencia en el archivo de registro y continúa con el resto de la instalación sin ningún error. Para obtener información, consulte [Uso de Windows Installer y Windows Resource Protection](windows-resource-protection-on-windows-vista.md).
-   WRP es el nuevo nombre de Windows File Protection (WFP). WRP protege las claves y carpetas del Registro, así como los archivos esenciales del sistema. En Windows Server 2003, Windows XP y Windows 2000, cuando el instalador de Windows encontró un archivo protegido por WFP, el instalador solicitaría que WFP instalara el archivo. Para obtener información, consulte [Uso de Windows Installer y Windows Resource Protection](windows-resource-protection-on-windows-vista.md).

## <a name="do-not-depend-upon-non-critical-resources"></a>No dependa de recursos no críticos.

La instalación o actualización no debe depender de la instalación de recursos no críticos por los siguientes motivos.

-   Las acciones personalizadas pueden producir un error si dependen de un componente que pertenezca a una característica que el usuario anuncia en lugar de instalar.
-   Las acciones personalizadas secuenciadas antes de la acción [InstallFinalize](installfinalize-action.md) pueden producir un error si dependen de un componente que contiene un ensamblado que se está instalando. El Windows no confirma ensamblados en la caché global de ensamblados (GAC) hasta que se complete la acción InstallFinalize.

## <a name="use-the-api-to-retrieve-windows-installer-configuration-information"></a>Use la API para recuperar Windows configuración del instalador.

La instalación de la aplicación o actualización no debe depender del acceso directo a Windows de configuración del instalador guardado en el equipo. En su lugar, use la interfaz Windows programación de aplicaciones del instalador para recuperar información de configuración. La ubicación y el formato de la información de configuración se administran mediante Windows Installer y pueden cambiar.

-   Las funciones de instalación y configuración de la API Windows Installer se describen en [la Referencia de función del instalador](installer-function-reference.md).
-   Las [propiedades de configuración](property-reference.md) se describen en la Referencia de propiedades.
-   Los métodos y propiedades de automatización se describen en la referencia [de la interfaz de Automation](automation-interface-reference.md). El script de WiLstPrd.vbs se conecta a un objeto Installer y enumera los productos registrados y la información del producto. Para obtener información, [vea Enumerar productos, propiedades, características y componentes.](list-products-properties-features-and-components.md)

## <a name="organize-the-installation-of-your-application-around-components"></a>Organice la instalación de la aplicación en torno a los componentes.

El Windows installer instala o quita colecciones de recursos denominados [componentes](windows-installer-components.md). Dado que los componentes se comparten normalmente, el autor de un paquete de instalación debe seguir las reglas al especificar los componentes de una característica o aplicación.

-   Cumpla las reglas [](organizing-applications-into-components.md) de componentes al organizar las aplicaciones en componentes para asegurarse de que los nuevos componentes, o las nuevas versiones de los componentes, se pueden instalar y quitar sin dañar otras aplicaciones. Puede seguir el procedimiento descrito en [Definición de componentes del instalador](defining-installer-components.md).
-   El instalador realiza un seguimiento de cada componente por el GUID del identificador de componente correspondiente especificado en la [tabla Component](component-table.md). Para el funcionamiento del mecanismo de recuento de referencias Windows installer, es fundamental que el GUID del identificador de componente sea correcto. Siga las instrucciones de [Cambio del código de componente](changing-the-component-code.md).
-   Si el paquete debe interrumpir las reglas de componentes, tenga en cuenta las posibles consecuencias y asegúrese de que la instalación nunca instale estos componentes donde puedan dañar los componentes del sistema del usuario. Para obtener información, [vea ¿Qué ocurre si se han](what-happens-if-the-component-rules-are-broken.md)roto las reglas de componente? .
-   Tenga en cuenta cómo el Windows de archivos aplica las reglas de [control](file-versioning-rules.md) de versiones de [archivos al reemplazar archivos existentes.](replacing-existing-files.md) El Windows de instalación determina primero si el archivo de clave del componente ya está instalado antes de intentar instalar cualquiera de los archivos del componente. Si el instalador encuentra un archivo con el mismo nombre que el archivo de clave del componente instalado en la ubicación de destino, compara la versión, la fecha y el idioma de los dos archivos clave y usa reglas de control de versiones de archivos para determinar si se debe instalar el componente proporcionado por el paquete. Si el instalador determina que debe reemplazar el componente en función del archivo de clave, usa las reglas de control de versiones de archivo en cada archivo instalado para determinar si se debe reemplazar el archivo.

## <a name="reduce-the-size-of-large-windows-installer-packages"></a>Reduzca el tamaño de los paquetes Windows Installer.

Los paquetes Windows grandes toman recursos del sistema y pueden ser difíciles de instalar para los usuarios. Es una buena práctica reducir el tamaño de los paquetes Windows instalador mediante los métodos siguientes.

-   Comprima los archivos de la instalación y almacéne en un archivo de archivador (.cab). El instalador permite que .cab archivo se almacene como un archivo externo independiente o como un flujo de datos en el propio paquete MSI. Para obtener [información, vea Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).
-   Quite el espacio de almacenamiento desperdiciado en el archivo .msi mediante una de las opciones que se deba en [Reducción](reducing-the-size-of-an--msi-file.md)del tamaño de un .msi archivo .
-   Si el Windows installer contiene más de 32767 archivos, debe cambiar el esquema de la base de datos. Para obtener [información, vea Creación de un paquete grande.](authoring-a-large-package.md)

## <a name="if-you-use-custom-actions-follow-good-custom-action-practices"></a>Si usa acciones personalizadas, siga los procedimientos de acción personalizados recomendados.

El Windows programa de instalación tiene muchas acciones estándar [integradas](standard-actions-reference.md) para la instalación y el mantenimiento de las aplicaciones. Los desarrolladores deben intentar confiar en las acciones estándar tanto como sea práctico, en lugar de crear sus [propias acciones personalizadas.](custom-actions.md) Sin embargo, hay situaciones en las que el desarrollador de un paquete de instalación encuentra necesario escribir una acción personalizada.

-   Siga las instrucciones de [Uso de acciones personalizadas.](using-custom-actions.md)
-   Siga las [directrices para proteger las acciones personalizadas.](guidelines-for-securing-custom-actions.md) Las acciones personalizadas que usan información confidencial no deben escribir esta información en el registro. Para obtener información, [vea Custom Action Security](custom-action-security.md).
-   Las acciones personalizadas no deben intentar establecer un Restaurar sistema de entrada desde dentro de una acción personalizada. Para obtener información, [vea Establecer un punto de restauración a partir de una acción personalizada.](setting-a-restore-point-from-a-custom-action.md)
-   Devuelva mensajes de error de acciones personalizadas y escríbalos en el registro para facilitar la solución de problemas de acciones personalizadas. Para obtener información, [vea Acciones personalizadas de mensajes de error](error-message-custom-actions.md) y Devolver mensajes de error de acciones [personalizadas.](returning-error-messages-from-custom-actions.md)
-   No cambie el estado del sistema de una acción personalizada inmediata. Las acciones personalizadas que cambian el sistema directamente o llaman a otro servicio del sistema deben aplazarse hasta el momento en que se ejecuta el script de instalación. Cada [acción personalizada de ejecución](deferred-execution-custom-actions.md) diferida que cambia [](rollback-custom-actions.md) el estado del sistema debe ir precedida de una acción personalizada de reversión para deshacer el cambio de estado del sistema en una reversión de la instalación. Para obtener [información, vea Cambiar el estado del sistema mediante una acción personalizada.](changing-the-system-state-using-a-custom-action.md)
-   Las acciones personalizadas que realizan operaciones de instalación complejas deben ser [un archivo ejecutable o](executable-files.md) una biblioteca de [vínculos dinámicos.](dynamic-link-libraries.md) Limite el uso de acciones personalizadas basadas en [scripts a](scripts.md) operaciones de instalación sencillas.
-   Haga que los administradores del sistema puedan detectar fácilmente los detalles de lo que hace la acción personalizada en el sistema. Coloque los detalles de las entradas y los archivos del Registro que usa la acción personalizada en una tabla personalizada y haga que la acción personalizada se lea de esta tabla. Esto se muestra en el ejemplo de [Usar una acción personalizada para crear cuentas de usuario en un equipo local.](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md) Para obtener información sobre cómo agregar tablas personalizadas a una base de datos, vea [Trabajar](working-with-queries.md) con consultas y ejemplos de consultas de base de datos [SQL script](examples-of-database-queries-using-sql-and-script.md).
-   Las acciones personalizadas no deben mostrar un cuadro de diálogo. Las acciones personalizadas que requieren una interfaz de usuario pueden usar la [**función MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) en su lugar. Consulte [Envío de mensajes a Windows instalador mediante MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).
-   Las acciones personalizadas no deben usar ninguna de las funciones enumeradas en la página: [Funciones no para su uso en acciones personalizadas.](functions-not-for-use-in-custom-actions.md)
-   Si la instalación está pensada para ejecutarse en un servidor de Terminal Server, pruebe que todas las acciones personalizadas son capaces de ejecutarse en un servidor terminal. Para obtener más información, [**vea TerminalServer, propiedad.**](terminalserver.md)
-   Para que una acción personalizada se ejecute cuando se desinstale una revisión determinada, la acción personalizada debe estar presente en la aplicación original o estar en una revisión para el producto que siempre se aplica. Para obtener más información, [vea Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).
-   Las acciones personalizadas no deben usar el nivel de interfaz de usuario como condición para enviar mensajes de error al instalador, ya que esto puede interferir con el registro y los mensajes externos. Para obtener información, [vea Determinar el nivel de interfaz de usuario a partir de una acción personalizada.](determining-ui-level-from-a-custom-action.md)
-   Use instrucciones condicionales y sintaxis de instrucciones condicionales para asegurarse de que el paquete ejecuta correctamente acciones personalizadas, no ejecuta acciones personalizadas o ejecuta una acción personalizada alternativa cuando se desinstala el paquete. [](conditional-statement-syntax.md) Compruebe que el paquete funciona según lo previsto al [desinstalar acciones personalizadas.](uninstalling-custom-actions.md) Para obtener información, [vea Acciones de asemiento que se ejecutarán durante la eliminación.](conditioning-actions-to-run-during-removal.md)
-   Si la instalación debe ser capaz de ser ejecutada por usuarios que no tienen privilegios de administrador, pruebe para asegurarse de que todas las acciones personalizadas se pueden ejecutar con privilegios que no son de administrador. Las acciones personalizadas requieren privilegios elevados para modificar partes del sistema que no son específicas del usuario. El instalador puede ejecutar acciones personalizadas con privilegios elevados si se instala una aplicación administrada o si se ha especificado la directiva del sistema para privilegios elevados. Todas las acciones personalizadas que requieran privilegios elevados deben incluir msidbCustomActionTypeInScript y msidbCustomActionTypeNoImpersonate [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md) en el tipo de acción personalizada. Esto se muestra en el ejemplo de [Usar una acción personalizada para crear cuentas de usuario en un equipo local.](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)

## <a name="if-you-use-assemblies-follow-good-assembly-practices"></a>Si usa ensamblados, siga los procedimientos de ensamblado recomendados.

Si el paquete usa ensamblados de [software](assemblies.md), siga las instrucciones para Agregar ensamblados [a](adding-assemblies-to-a-package.md)un paquete [,](updating-assemblies.md)Actualizar ensamblados e Instalar y [quitar ensamblados](installing-and-removing-assemblies.md).

## <a name="do-not-ship-concurrent-installations"></a>No envíe instalaciones simultáneas.

[Instalaciones simultáneas](concurrent-installations.md), también denominadas instalaciones anidadas, instale otro paquete Windows Installer durante una instalación en ejecución actualmente. El uso de instalaciones simultáneas no es un procedimiento recomendado porque son difíciles de dar servicio a los clientes. Es posible que la aplicación de revisiones y la actualización no funcionen con instalaciones simultáneas. La alternativa recomendada al uso de instalaciones simultáneas es usar en su lugar una aplicación de instalación y un controlador de interfaz de usuario externo para instalar varios paquetes Windows Installer secuencialmente.

Para obtener más información sobre el uso de un controlador de interfaz de usuario externo, vea [Supervisar una instalación mediante MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md). Para obtener más información sobre el uso de un controlador externo basado en registros, vea Supervisar una instalación [mediante MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).

A veces, las instalaciones simultáneas se usan en entornos corporativos controlados para instalar aplicaciones que no están diseñadas para el público. Siga estas instrucciones si decide usar instalaciones simultáneas.

-   No use instalaciones simultáneas para instalar o actualizar un producto de envío.
-   Las instalaciones simultáneas no deben compartir componentes.
-   Una instalación administrativa no debe contener una instalación simultánea.
-   Las barras de progreso integradas no deben usarse con instalaciones simultáneas.
-   Los recursos que se van a anunciar no deben instalarse mediante una instalación simultánea.
-   Un paquete que realiza una instalación simultánea de una aplicación también debe desinstalar la aplicación simultánea cuando se desinstala el producto primario. Existe una instalación anidada en el contexto del producto primario en agregar o quitar programas en Panel de control.

## <a name="keep-package-names-and-package-codes-consistent"></a>Mantener los nombres de paquete y los códigos de paquete coherentes.

Al .msi se le puede dar cualquier nombre que ayude a los usuarios a identificar el paquete, pero el nombre no debe cambiarse sin cambiar también el código del producto.

-   Asigne al .msi un nombre descriptivo que permita al usuario identificar el contenido del paquete Windows Installer.
-   El [código de producto](product-codes.md) es la identificación principal de una aplicación y debe cambiar siempre que haya una actualización completa de la aplicación. Para obtener información, [**vea ProductCode**](productcode.md) y [Cambio del código de producto.](changing-the-product-code.md) Cambiar el nombre del archivo de .msi aplicación se considera un cambio completo y siempre requiere un cambio correspondiente del código de producto para mantener la coherencia.
-   El [código del paquete](package-codes.md) es el identificador principal utilizado por el instalador para buscar y validar el paquete correcto para una instalación determinada. Dos archivos de .msi no identificados nunca deben tener el mismo código de paquete. Si se cambia un paquete sin cambiar el código del paquete, es posible que el instalador no use el paquete más reciente si ambos siguen siendo accesibles para el instalador. El código del paquete se almacena en la [**propiedad Resumen del**](revision-number-summary.md) número de revisión del flujo de información de [resumen](summary-information-stream.md).
-   Tenga en cuenta que las letras del código de producto y los GUID del código [de paquete deben](guid.md) estar en mayúsculas.

## <a name="do-not-use-the-selfreg-and-typelib-tables"></a>No use las tablas SelfReg y TypeLib.

-   Se recomienda encarecidamente a los autores de paquetes de instalación que no utilicen el registro propio y la [tabla SelfReg.](selfreg-table.md) En su lugar, deben registrar módulos mediante la creación de una o varias de las tablas en el grupo [Tablas del Registro](registry-tables-group.md). Muchas de las ventajas del instalador de Windows se pierden con el registro automático porque las rutinas de registro automático tienden a ocultar información de configuración crítica. Para obtener una lista de las razones para evitar el registro propio, consulte [la tabla SelfReg](selfreg-table.md).
-   Se recomienda encarecidamente a los autores de paquetes de instalación que no utilicen [la tabla TypeLib.](typelib-table.md) En lugar de usar la tabla TypeLib, registre bibliotecas de tipos mediante [la tabla registry.](registry-table.md) Si se produce un error en una instalación que usa la tabla TypeLib y se debe revertir, es posible que la reversión no restaure el equipo al mismo estado que existía antes de la reversión.

## <a name="provide-the-option-to-install-without-a-user-interface"></a>Proporcione la opción para instalar sin una interfaz de usuario.

A menudo, los administradores prefieren implementar aplicaciones dentro de una empresa sin necesidad de la interacción del usuario. Es un procedimiento recomendado permitir que la aplicación proporcione la opción de instalarse con el nivel [de interfaz de usuario](user-interface-levels.md) Ninguno.

-   Use [propiedades públicas para](public-properties.md) obtener información de configuración. Los administradores pueden proporcionar esta información en la línea de comandos.
-   No es necesario que la instalación dependa de la información recopilada de la interacción del usuario con los cuadros de diálogo. Esta información no está disponible durante una instalación silenciosa.
-   No reinicie automáticamente el equipo del usuario durante una instalación silenciosa.
-   Los administradores pueden establecer el [nivel de interfaz de usuario](user-interface-levels.md) al instalar mediante la opción de línea de [comandos](command-line-options.md) "/q". El nivel de interfaz de usuario también se puede establecer mediante programación con una llamada a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).

## <a name="avoid-using-the-alwaysinstallelevated-policy"></a>Evite usar la directiva AlwaysInstallElevated.

Si no se establece la directiva [AlwaysInstallElevated,](alwaysinstallelevated.md) las aplicaciones no distribuidas por el administrador se instalan con los privilegios del usuario y solo las aplicaciones administradas obtienen privilegios elevados. Al establecer esta directiva, Windows instalador use permisos del sistema al instalar la aplicación en el sistema. Este método puede abrir un equipo con un riesgo de seguridad, ya que [](e-gly.md) cuando se establece esta directiva, un usuario que no es administrador puede ejecutar instalaciones con privilegios elevados y acceder a ubicaciones seguras en el equipo. Es un procedimiento recomendado usar otro método que no sea la directiva AlwaysInstallElevated al instalar un paquete con [privilegios elevados](installing-a-package-with-elevated-privileges-for-a-non-admin.md) para un usuario que no es administrador o que no Per-User [aplicaciones administradas.](patching-per-user-managed-applications.md)

## <a name="enable-the-disablemedia-policy-to-limit-unauthorized-installation"></a>Habilite la directiva DisableMedia para limitar la instalación no autorizada.

La [directiva DisableMedia](disablemedia.md) puede impedir la instalación no autorizada de aplicaciones. Cuando esta directiva está habilitada, se impide que los usuarios y administradores que ejecutan una instalación de mantenimiento de un producto usen el cuadro de diálogo Examinar para examinar los orígenes multimedia, como CD-ROM, para los orígenes de otros productos instalables. La exploración de otros productos se impide independientemente de si la instalación se realiza con privilegios elevados. Todavía es posible que el usuario vuelva a instalar el producto desde un medio si el usuario tiene un origen multimedia etiquetado correctamente.

## <a name="keep-the-original-package-source-files-secure-and-available-to-users"></a>Mantenga los archivos de origen del paquete original seguros y disponibles para los usuarios.

En algunos casos, el origen original del paquete Windows Installer puede ser necesario para instalar, reparar o actualizar una aplicación a petición. Si el instalador no puede encontrar un origen disponible, se pide al usuario que proporcione medios o que vaya a una ubicación de red que contenga los orígenes necesarios. Es un procedimiento recomendado asegurarse de que el instalador tiene los orígenes que necesita sin tener que preguntar al usuario.

-   Use [firmas digitales y archivos de archivado externos](digital-signatures-and-external-cabinet-files.md) para asegurarse de que los orígenes origiales que usa el instalador son seguros. Una imagen de origen sin comprimir almacenada en una ubicación pública no es segura.
-   Incluya una lista completa de rutas de acceso de origen de red o dirección URL al paquete de instalación de la aplicación en la [**propiedad SOURCELIST.**](sourcelist.md)
-   Use un recurso compartido Sistema de archivos distribuido (DFS) para la ruta de acceso de origen.
-   Use la API Windows Installer para recuperar y modificar la información de la lista de origen Windows aplicaciones y revisiones del instalador. Para obtener información, [vea Administración de orígenes de instalación.](managing-installation-sources.md)
-   Use los métodos y las [](product-object.md)propiedades del [](patch-object.md) objeto del [**instalador,**](installer-object.md)el objeto de producto y el objeto de revisión para recuperar y modificar la información de la lista de origen para Windows aplicaciones y revisiones del instalador.
-   Siga los puntos enumerados en [Impedir que](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md) una revisión requiera acceso a los puntos de origen de instalación original para minimizar la posibilidad de que la revisión requiera acceso a los orígenes originales.
-   Almacene los archivos de origen del paquete en una ubicación que no sea la carpeta temporal del sistema. Windows Los archivos de origen del instalador almacenados en la carpeta temporal pueden no estar disponibles para los usuarios.

## <a name="enable-verbose-logging-on-users-computer-when-troubleshooting-deployment"></a>Habilite el registro detallado en el equipo del usuario al solucionar problemas de implementación.

[Windows registro del instalador](windows-installer-logging.md) incluye una opción de registro detallada que se puede habilitar en el equipo de un usuario. La información de un registro detallado puede resultar útil al intentar solucionar problemas Windows implementación del paquete del instalador.

-   Puede habilitar el registro detallado en el equipo del usuario mediante las opciones de la línea de comandos [,](command-line-options.md)la propiedad [**MsiLogging,**](msilogging.md) la directiva de registro [,](logging.md) [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)y el [**método EnableLog.**](installer-enablelog.md)
-   Un recurso muy útil para interpretar los Windows de registro del instalador es [Wilogutl.exe](wilogutl-exe.md). Esta herramienta ayuda al análisis de archivos de registro y muestra soluciones sugeridas a los errores que se encuentran en un archivo de registro.
-   Para obtener más información sobre cómo interpretar Windows archivos de registro del instalador, consulte las white paper disponibles en el sitio de TechNet: [Windows Installer: Benefits and Implementation for System Administrators](https://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/winmsi.mspx).
-   La opción de registro detallado solo debe usarse con fines de solución de problemas y no se debe dejar activa porque puede tener efectos negativos en el rendimiento del sistema y el espacio en disco. Cada vez que se usa la herramienta Agregar o quitar programas Panel de control, se crea un nuevo archivo.

## <a name="uninstallation-leaves-the-users-computer-in-a-clean-state"></a>La desinstalación deja el equipo del usuario en un estado limpio.

La eliminación de aplicaciones es tan importante como la instalación. Cuando se desinstala Windows paquete del instalador, no debe dejar ninguna parte inutil de sí misma en el equipo del usuario.

-   Si un archivo que se debe haber quitado del equipo del usuario permanece instalado después de ejecutar una desinstalación, es posible [](removing-stranded-files.md)que el instalador no quite el componente que contiene el archivo por una o varias de las razones descritas en Eliminación de archivos desenlazados.
-   Si se debe registrar una aplicación, cree el paquete para quitar la información del Registro cuando se desinstale la aplicación. Para obtener [información, vea Agregar o quitar claves del Registro en la instalación o eliminación de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). Si una aplicación no está registrada, la aplicación no aparece en la característica Agregar o quitar programas de Panel de control y no se puede administrar mediante el instalador de Windows.
-   Para ocultar una aplicación de la característica Agregar o quitar programas de Panel de control y seguir siendo capaz de usar el instalador de Windows para administrar la aplicación, siga las instrucciones descritas en Agregar y quitar una aplicación y dejar [ningún](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)seguimiento en el Registro .
-   Las acciones personalizadas deben estar condiciones para ejecutarse o no según sea necesario tras la desinstalación. Es posible que sea necesario ejecutar diferentes acciones personalizadas al instalar y desinstalar.
-   La información de personalización específica del usuario se puede almacenar en un archivo de texto en el equipo. Esto tiene la ventaja de que el archivo se puede quitar cuando se desinstala la aplicación, incluso si el usuario de esta personalización no ha iniciado sesión actualmente.

## <a name="test-packages-for-both-per-user-and-per-machine-installation-deployment"></a>Pruebe los paquetes para la implementación de instalación por usuario y por máquina.

Es un procedimiento recomendado permitir que los clientes decidan si implementar un paquete para la instalación en el contexto de instalación por equipo o [por usuario](installation-context.md).

-   Considere si la aplicación debe estar disponible solo para usuarios concretos o para todos los usuarios del equipo durante el proceso de desarrollo.
-   Compruebe que el paquete funciona correctamente para los contextos de instalación por usuario y por equipo.
-   Haga que el paquete sea fácilmente personalizable y permita que los clientes decidan si implementarlo por usuario o por equipo.

## <a name="plan-and-test-a-servicing-strategy-before-shipping-the-application"></a>Planee y pruebe una estrategia de mantenimiento antes de enviar la aplicación.

Debe decidir cómo piensa dar servicio a la aplicación antes de implementarla por primera vez.

-   Tenga en cuenta los tipos de actualizaciones que espera usar para dar servicio a la aplicación en el futuro. El Windows proporciona tres tipos de [actualizaciones:](small-updates.md)actualización pequeña, actualización [secundaria](minor-upgrades.md)y [actualizaciones principales.](major-upgrades.md) Las diferencias entre ellas se describen en [el tema Aplicación de revisiones y](patching-and-upgrades.md) actualizaciones.
-   Antes de enviar la aplicación, compruebe que funciona según lo previsto después de realizar el mantenimiento con cada tipo de actualización.

## <a name="reduce-the-dependency-of-updates-upon-the-original-sources"></a>Reduzca la dependencia de las actualizaciones en los orígenes originales.

Si los archivos de origen originales son necesarios para actualizar la aplicación, esto puede dificultar el mantenimiento de la aplicación. Los métodos siguientes pueden ayudar a reducir la dependencia de las actualizaciones en los orígenes originales.

-   Use una [*revisión diferencial para*](d-gly.md) actualizar las versiones de línea base de la aplicación, como la versión RTM y las versiones de Service Pack. Siga las instrucciones para usar las revisiones diferenciales que se describen en el tema [Reducción del tamaño de revisión.](reducing-patch-size.md)
-   Siga las recomendaciones enumeradas en el tema: Impedir que una [revisión requiera acceso al origen de instalación original](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

## <a name="do-not-distribute-unserviceable-merge-modules"></a>No distribuya módulos de combinación que no son de servicio.

Las aplicaciones no deben depender de [los módulos de](merge-modules.md) combinación para la instalación del componente si el propietario del módulo de mezcla y el propietario de la aplicación son diferentes. Esto puede dificultar el servicio de la aplicación porque ambos propietarios deben coordinarse para actualizar la aplicación o el módulo. Sin conocer todas las aplicaciones que han usado el módulo de combinación, el propietario de la aplicación no puede actualizar el módulo de combinación sin riesgo de que la actualización pueda ser incompatible con otra aplicación. El propietario del módulo de combinación no tiene ningún método directo para actualizar Windows paquetes del instalador que ya han instalado el módulo de combinación.

-   Considere la posibilidad de proporcionar los componentes necesarios a los usuarios como otra instalación Windows instalador.

## <a name="avoid-patching-administrative-installations"></a>Evite aplicar revisiones a las instalaciones administrativas.

Proporcione en una red una [instalación administrativa](administrative-installation.md) del paquete Windows Installer original de la aplicación para permitir que los miembros de un grupo de trabajo instalen la aplicación. A continuación, los usuarios de esta imagen administrativa deben aplicar actualizaciones a la instancia local de la aplicación ubicada en su equipo. Esto mantiene a los usuarios en sincronización con la imagen administrativa. No se recomienda aplicar actualizaciones a la instalación administrativa por los siguientes motivos.

-   El tamaño y la latencia de la descarga necesarias para que los usuarios obtengan una actualización aumenta en comparación con la descarga de una revisión. Todos los archivos de origen y Windows del instalador actualizados deben descargarse, volver a almacenarse en caché y reinstalarse.
-   Los usuarios no pueden [instalar a petición](installation-on-demand.md) ni reparar aplicaciones desde una instalación administrativa actualizada hasta que vuelvan a almacenar en caché y reinstalar la aplicación.
-   Al aplicar una revisión a una instalación administrativa, se quita la firma digital del paquete. Un administrador debe volver a presentar el paquete. Para obtener más información sobre el uso de firmas digitales, vea [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md)(Firmas digitales y Windows instalador).
-   Muchas revisiones binarias tienen como destino la imagen RTM de la aplicación y requieren una versión de archivo anterior. Es posible que la instancia local de una aplicación instalada desde una instalación administrativa actualizada no funcione con otras actualizaciones. Muchas aplicaciones de revisión binaria pueden producir errores.
-   Al aplicar una revisión a una instalación administrativa, se actualizan los archivos de origen y el archivo .msi, pero no se marca la imagen de red con información sobre la actualización. Los usuarios no pueden determinar qué actualizaciones han recibido de la instalación administrativa. Esto hace imposible secuenciar las actualizaciones aplicadas en el lado del usuario con las que ya se han aplicado en el lado de la imagen administrativa.
-   Las revisiones aplicadas a una instalación administrativa no son [revisiones que se pueden desinstalar.](uninstallable-patches.md) Esto puede impedir que el código del paquete almacenado en caché en el equipo del usuario sea diferente del código del paquete en la instalación administrativa. Si el código del paquete almacenado en caché en el equipo del usuario es diferente del de la instalación administrativa, vuelva a instalar la aplicación desde la instalación administrativa y, a continuación, vuelva a aplicar revisiones al equipo cliente.
-   Si decide aplicar actualizaciones pequeñas mediante la aplicación de revisiones a una imagen administrativa, siga las instrucciones descritas en el tema: Aplicar pequeñas actualizaciones mediante la aplicación de revisiones [a una imagen administrativa.](applying-small-updates-by-patching-an-administrative-image.md)

## <a name="register-updates-to-run-with-elevated-privilege"></a>Registre las actualizaciones para que se ejecuten con privilegios elevados.

A partir de Windows Installer 3.0, es posible aplicar revisiones a una aplicación que se ha instalado en un contexto administrado por usuario, después de que la revisión se haya registrado como con privilegios elevados. No se pueden aplicar revisiones a las aplicaciones instaladas en un contexto administrado por usuario mediante versiones de Windows Installer anteriores a la versión 3.0.

-   Use el [**método SourceListAddSource**](patch-sourcelistaddsource.md) o la [**función MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para registrar un paquete de revisión con privilegios elevados. Siga las instrucciones y ejemplos proporcionados en [Aplicación de revisiones Per-User Aplicaciones administradas](patching-per-user-managed-applications.md).
-   Al ejecutar Windows Installer versión 4.0 en Windows Vista, también puede usar la aplicación de revisiones de control de cuentas de usuario [(UAC)](user-account-control--uac--patching.md) para que los autores de las instalaciones del instalador de Windows identifiquen las revisiones firmadas digitalmente que los usuarios que no son administradores pueden aplicar en el futuro. Esto solo está disponible con la instalación de paquetes en el contexto de instalación por [equipo](installation-context.md) (ALLUSERS=1).
-   Asegúrese de que la aplicación de revisiones con privilegios mínimos no se ha deshabilitado estableciendo la propiedad [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) o la [directiva DisableLUAPatching.](disableluapatching.md)

## <a name="use-the-msipatchsequence-table-to-sequence-patches"></a>Use la tabla MsiPatchSequence para secuenciar revisiones.

Incluya una [tabla MsiPatchSequence](msipatchsequence-table.md) en el paquete y agregue información de secuenciación de revisiones. A partir Windows installer versión 3.0, el instalador puede usar la [](installing-multiple-patches.md) tabla MsiPatchSequence al instalar varias revisiones para determinar la mejor secuencia de aplicación de revisiones. Use las instrucciones descritas en las notas del producto sobre la secuenciación de revisiones [en Windows Installer versión 3.0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3) para definir familias de revisiones.

-   Si es práctico, especifique todas las revisiones como pertenecientes a una sola familia de revisiones. En muchos casos, una sola familia de revisiones proporciona suficiente flexibilidad para secuenciar revisiones. La complejidad de la creación aumenta cuando se usan varias familias de revisiones. Asigne un nombre descriptivo a la familia de revisiones y asigne valores de secuencia en esa familia de revisiones que aumenten con el tiempo. Siga el [ejemplo de varias revisiones](multiple-patching-example.md) para aplicar revisiones en el orden en que se han emitido.
-   Use la [tabla PatchSequence de](patchsequence-table--patchwiz-dll-.md) [Patchwiz.dll](patchwiz-dll.md) para generar la información [en MsiPatchSequence Table](msipatchsequence-table.md). La versión de PATCHWIZ.DLL que se publicó con Windows Installer 3.0 puede generar automáticamente información de secuenciación de revisiones. Para obtener más información sobre cómo agregar una nueva revisión, vea [Generar información de secuencia de revisión.](generating-patch-sequence-information---patchwiz-dll-.md) Para obtener más información sobre los escenarios de secuenciación de revisiones, vea las notas del producto: Secuenciación de revisiones [en Windows Installer versión 3.0.](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3)

## <a name="test-the-installation-package-thoroughly"></a>Pruebe el paquete de instalación exhaustivamente.

Pruebe la instalación, reparación y eliminación correctas del paquete Windows Installer. Puede dividir el proceso de pruebas en las siguientes partes.

-   Pruebas de instalación: pruebe la instalación con todas las combinaciones posibles de características de la aplicación. Pruebe todos los tipos de instalación, incluida [la instalación administrativa,](administrative-installation.md) [la instalación de](rollback-installation.md)reversión y la instalación a [petición.](installation-on-demand.md) Pruebe todos los métodos posibles de instalación, incluido hacer clic en el archivo [.msi,](command-line-options.md)las opciones de línea de comandos e instalar desde el panel de control. Compruebe que los usuarios pueden instalar el paquete en todos los contextos de privilegios posibles. Intente instalar el paquete una vez implementado por todos los métodos posibles. Habilite [Windows del instalador para](windows-installer-logging.md) cada prueba y resuelva todos los errores encontrados en el registro del instalador y el registro de eventos.
-   Interfaz de usuario Testing: pruebe el paquete cuando se instale con todos los niveles de [interfaz de usuario posibles.](user-interface-levels.md) Pruebe el paquete instalado sin interfaz de usuario y con toda la información proporcionada a través de la interfaz de usuario. Asegúrese de [la accesibilidad de](accessibility.md) la interfaz de usuario y de que la interfaz de usuario funcione según lo previsto para diferentes resoluciones de pantalla y tamaños de fuente.
-   Pruebas de mantenimiento y reparación: compruebe que el paquete puede controlar [](minor-upgrades.md)las revisiones y actualizaciones [entregadas](patching-and-upgrades.md) por una actualización [pequeña,](small-updates.md)una actualización secundaria y [actualizaciones principales.](major-upgrades.md) Antes de implementar el paquete, escriba una actualización de prueba de cada tipo e intente aplicarlo al paquete original.
-   Pruebas de desinstalación: compruebe que, cuando se quita el paquete, no deja partes inutiles de sí mismo en el equipo del usuario y que solo se ha quitado la información que pertenece al paquete. Reinicie el equipo de prueba después de desinstalar el paquete y compruebe la integridad de las herramientas comunes del sistema y otras aplicaciones estándar. Compruebe que los usuarios pueden quitar el paquete en todos los contextos de privilegios posibles. Pruebe todos los métodos para quitar el paquete, [](command-line-options.md)haga clic en el archivo .msi, pruebe las opciones de la línea de comandos e intente quitar el paquete del panel de control. Habilite [Windows del instalador para](windows-installer-logging.md) cada prueba y resuelva todos los errores encontrados en el registro del instalador y el registro de eventos.
-   Pruebas de funcionalidad del producto: asegúrese de que la aplicación funciona según lo previsto después de la instalación, reparación o eliminación del paquete.

## <a name="fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package"></a>Corrija todos los errores de validación antes de implementar un paquete de instalación nuevo o revisado.

Ejecute [la validación de](package-validation.md) paquetes en un paquete Windows installer nuevo o revisado antes de intentar instalarlo por primera vez. La validación comprueba si la Windows instalador de errores de creación. Si se intenta instalar un paquete que no pasa la validación, se puede dañar el sistema del usuario.

-   Puede validar el paquete [ mediante ](orca-exe.md)Orca.exeo [Msival2.exe](msival2-exe.md). Ambas herramientas se proporcionan con Windows SDK. Los proveedores de terceros también pueden incorporar el sistema de validación de ICE en su entorno de creación.
-   Puede usar el conjunto estándar de evaluadores de coherencia interna: TIC incluidos en los archivos .uu [proporcionados](internal-consistency-evaluators-ices.md) con el SDK, o bien personalizar la validación mediante la creación de un [ICE](building-an-ice.md) y su incorporación al archivo .uu.
-   Puede usar el Evalcom2.dll para implementar la automatización de [validación](validation-automation.md) para los paquetes de instalación y los módulos de combinación.

## <a name="author-a-secure-installation"></a>Cree una instalación segura.

Sigue estas instrucciones al desarrollar el paquete para ayudar a mantener un entorno seguro durante la instalación.

-   [Directrices para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md)
-   [Directrices para proteger paquetes en equipos bloqueados](guidelines-for-securing-packages-on-locked-down-computers.md)
-   [Directrices para proteger acciones personalizadas](guidelines-for-securing-custom-actions.md)

## <a name="use-pmsihandle-instead-of-handle"></a>Usar PMSIHANDLE en lugar de HANDLE

Las **variables de tipo PMSIHANDLE** se definen en msi.h. Se recomienda que la aplicación use el tipo **PMSIHANDLE** porque el instalador cierra objetos **PMSIHANDLE** a medida que sale del ámbito, mientras que la aplicación debe cerrar objetos **MSIHANDLE** mediante una llamada a [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).

Por ejemplo, si usa código como este:

``` syntax
MSIHANDLE hRec = MsiCreateRecord(3);
```

Cámbielo a:

``` syntax
PMSIHANDLE hRec = MsiCreateRecord(3);
```

 

 
