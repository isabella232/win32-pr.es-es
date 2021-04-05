---
description: Para habilitar Windows Installer en la aplicación, debe usar las funciones del instalador. En las tablas de este tema se identifican las funciones por categoría.
ms.assetid: 05a16915-6b47-4d51-b62a-5a4d92b87e50
title: Referencia de funciones del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9261789f21bd559e49c4e5718ef68ce9d0bb41c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001169"
---
# <a name="installer-function-reference"></a>Referencia de funciones del instalador

Para habilitar Windows Installer en la aplicación, debe usar las funciones del instalador. En las tablas de este tema se identifican las funciones por categoría.

## <a name="user-interface-and-logging-functions"></a>Funciones de interfaz de usuario y registro



| Nombre                                                     | Descripción                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)             | Habilita la interfaz de usuario interna del instalador.                                 |
| [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)             | Habilita un controlador de interfaz de usuario externo que recibe los mensajes en formato de cadena. |
| [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) | Habilita un controlador de interfaz de usuario externo que recibe mensajes en formato de registro. |
| [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)                     | Establece el modo de registro para todas las instalaciones del proceso que realiza la llamada.                       |



 

## <a name="handle-management-functions"></a>Administrar funciones de administración



| Nombre                                             | Descripción                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)         | Cierra un identificador de instalación abierto.                           |
| [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) | Cierra todos los identificadores de instalación abiertos. No se utiliza para la limpieza. |



 

## <a name="installation-and-configuration-functions"></a>Funciones de instalación y configuración



| Nombre                                                                     | Descripción                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)                       | Anuncia un producto.                                                                                                                                                                                                        |
| [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)                   | Anuncia un producto.                                                                                                                                                                                                        |
| [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)                         | Copia un archivo de script de anuncio en las ubicaciones especificadas.                                                                                                                                                                    |
| [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)                           | Instala o quita una aplicación o un conjunto de aplicaciones.                                                                                                                                                                     |
| [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)                       | Instala o quita una aplicación o un conjunto de aplicaciones.                                                                                                                                                                     |
| [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)                   | Instala o quita una aplicación o un conjunto de aplicaciones. Se puede especificar una línea de comandos del producto.                                                                                                                            |
| [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)                       | Vuelve a instalar o repara una instalación de.                                                                                                                                                                                       |
| [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)                       | Configura el estado de instalación de una característica.                                                                                                                                                                                 |
| [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)                       | Valida o repara características.                                                                                                                                                                                               |
| [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)         | Instala los componentes que faltan.                                                                                                                                                                                                 |
| [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)                   | Instala archivos que faltan.                                                                                                                                                                                                      |
| [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)                         | Notifica y actualiza la información interna de Windows Installer con cambios en los SID de usuario. Disponible a partir de Windows Installer 3,1.                                                                                   |
| [**MsiProcessAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiprocessadvertisescripta)           | Procesa un archivo de script de anuncio en las ubicaciones especificadas.                                                                                                                                                                 |
| [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)                 | Agrega o reordena los orígenes de un parche o producto en un contexto especificado.                                                                                                                                                   |
| [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)             | Agrega o reordena los orígenes de un parche o producto en un contexto especificado. Crea una lista de origen para una revisión que no existe en un contexto especificado. Disponible en Windows Installer 3,0.                                |
| [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)             | Quita un origen existente para un producto o revisión en un contexto especificado. Disponible en Windows Installer 3,0.                                                                                                               |
| [**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)                   | Quita todos los orígenes existentes de un tipo de origen específico para una instancia de producto especificada.                                                                                                                                 |
| [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)               | Quita todos los orígenes existentes de un tipo de origen específico para una instancia de producto especificada. Disponible en Windows Installer 3,0.                                                                                            |
| [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)     | Quita el registro del origen actual del producto o revisión, que se registra como la propiedad "LastUsedSource". Esta función no afecta a la lista de orígenes registrados.                                      |
| [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) | Quita el registro del origen actual del producto o revisión, que se registra como la propiedad "LastUsedSource". Esta función no afecta a la lista de orígenes registrados. Disponible en Windows Installer 3,0. |
| [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)                     | Recupera información sobre la lista de origen de un producto o revisión en un contexto específico.                                                                                                                                    |
| [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)                     | Establece el origen usado más recientemente para un producto o revisión en un contexto especificado. Disponible en Windows Installer 3,0.                                                                                                       |
| [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)       | Enumera la lista de discos registrados para el origen de medios para una revisión o un producto. Disponible en Windows Installer 3,0.                                                                                                    |
| [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)           | Agrega o actualiza un disco del origen de medios de un producto o revisión registrados. Disponible en Windows Installer 3,0.                                                                                                            |
| [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)      | Quita un disco registrado existente en el origen de medios de un producto o revisión en un contexto específico. Disponible en Windows Installer 3,0.                                                                                |
| [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)             | Enumera los orígenes de la lista de origen de un producto o revisión especificado. Disponible en Windows Installer 3,0.                                                                                                              |



 

## <a name="component-specific-functions"></a>Funciones de Component-Specific



| Nombre                                                                     | Descripción                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)                         | Instala y devuelve la ruta de acceso completa del componente de un ensamblado.                                                                                                                                                                 |
| [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)                       | Instala y devuelve la ruta de acceso completa del componente de un componente.                                                                                                                                                                  |
| [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)     | Instala y devuelve la ruta de acceso completa del componente de un componente calificado.                                                                                                                                                        |
| [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) | Instala y devuelve la ruta de acceso completa del componente de un componente calificado publicado por un producto.                                                                                                                         |
| [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)                       | Devuelve la ruta de acceso completa o la clave del registro a un componente instalado.                                                                                                                                                              |
| [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)                   | Devuelve la ruta de acceso completa o la clave del registro a un componente instalado en todas las cuentas de usuario y el contexto de instalación. **[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** No compatible.<br/> |
| [**MsiLocateComponent**](/windows/desktop/api/Msi/nf-msi-msilocatecomponenta)                         | Devuelve la ruta de acceso completa a un componente instalado sin un código de producto.                                                                                                                                                       |
| [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)                 | Devuelve el estado instalado de un componente. Puede consultar componentes de una instancia de un producto instalado en cuentas de usuario distintas del usuario actual. Disponible en Windows Installer 3,0 o posterior.                        |



 

## <a name="application-only-functions"></a>Funciones de Application-Only



| Nombre                                             | Descripción                                                            |
|--------------------------------------------------|------------------------------------------------------------------------|
| [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) | Almacena información de usuario de un asistente para la instalación de.                   |
| [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)           | Incrementa el recuento de uso de una característica e indica el estado de la instalación. |
| [**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)       | Incrementa el recuento de uso de una característica e indica el estado de la instalación. |
| [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)   | Devuelve el código de producto mediante el código del componente.                         |



 

## <a name="system-status-functions"></a>Funciones de estado del sistema



| Nombre                                                             | Descripción                                                                                                                                                                                                                       |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)                       | Enumera los productos anunciados.                                                                                                                                                                                                   |
| [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)                   | Enumera todas las instancias de productos anunciados o instalados en un contexto especificado. Disponible en Windows Installer 3,0 o posterior.                                                                                    |
| [**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)         | Enumera los productos instalados actualmente con un código de actualización especificado.                                                                                                                                                          |
| [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)                       | Enumera las características publicadas.                                                                                                                                                                                                    |
| [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)                   | Enumera los componentes instalados.                                                                                                                                                                                              |
| [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)               | Enumera los componentes instalados en las cuentas de usuario y el contexto de instalación. **[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** No compatible.<br/>                                 |
| [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)                         | Enumera los clientes de un componente instalado.                                                                                                                                                                                 |
| [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)                     | Enumera los clientes de un componente instalado en todas las cuentas de usuario y el contexto de instalación. **[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** No compatible.<br/>                    |
| [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) | Enumera los calificadores anunciados para un componente.                                                                                                                                                                             |
| [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)             | Devuelve el estado de instalación de una característica.                                                                                                                                                                                         |
| [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)         | Devuelve el estado instalado de una característica del producto. Puede consultar características de una instancia de un producto instalado en cuentas de usuario distintas del usuario actual. Disponible en Windows Installer 3,0 o posterior.                        |
| [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)             | Devuelve el estado de instalación de una aplicación o conjunto de aplicaciones.                                                                                                                                                              |
| [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)                 | Devuelve las métricas de uso de una característica.                                                                                                                                                                                              |
| [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)                   | Devuelve información del producto para los productos publicados e instalados.                                                                                                                                                                 |
| [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)               | Devuelve información del producto de los productos de anunciados e instalados. Puede recuperar información sobre una instancia de un producto instalado en una cuenta de usuario que no sea el usuario actual. Disponible en Windows Installer 3,0 o posterior. |
| [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)                         | Devuelve información de usuario registrada para un producto instalado.                                                                                                                                                                     |



 

## <a name="product-query-functions"></a>Funciones de consulta de productos



| Nombre                                                               | Descripción                                                                            |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)                           | Abre un producto para usarlo con las funciones que tienen acceso a la base de datos.                    |
| [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)                           | Abre un paquete para usarlo con las funciones que tienen acceso a la base de datos.                    |
| [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)                       | Abre un paquete para usarlo con las funciones que tienen acceso a la base de datos.                    |
| [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)               | Comprueba si el producto está instalado con privilegios elevados.                      |
| [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) | Devuelve información del producto para un archivo de script del instalador.                              |
| [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)             | Recupera propiedades en la base de datos del producto.                                          |
| [**MsiGetShortcutTarget**](/windows/desktop/api/Msi/nf-msi-msigetshortcuttargeta)               | Examina un acceso directo y devuelve su producto, nombre de característica y componente si está disponible. |
| [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)                     | Devuelve información descriptiva de una característica.                                         |
| [**MsiVerifyPackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)                       | Comprueba si un archivo especificado es un paquete de instalación.                             |



 

## <a name="patching-functions"></a>Funciones de revisión



| Nombre                                                                   | Descripción                                                                                                                                                        |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)                                 | Invoca una instalación y aplica un paquete de revisión.                                                                                                               |
| [**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)                    | Devuelve el GUID para cada revisión que se aplica a un producto y una lista de transformaciones de cada revisión que se aplican al producto.                                  |
| [**MsiGetPatchInfo**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoa)                             | Devuelve información acerca de una revisión.                                                                                                                                 |
| [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)                           | Desinstala una revisión de un producto. Disponible en Windows Installer 3,0.                                                                                             |
| [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)         | Determina la mejor secuencia de aplicación para un conjunto de revisiones y productos. Disponible en Windows Installer 3,0.                                                     |
| [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)             | Aplica una o más revisiones a los productos. Disponible en Windows Installer 3,0.                                                                                       |
| [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)                           | Enumera todas las revisiones aplicadas para un producto en un contexto determinado o en todos los contextos. Disponible en Windows Installer 3,0.                                   |
| [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)                     | Cuando se proporciona una lista de archivos. MSP, esta función recupera la lista de archivos que las revisiones pueden actualizar para el tino. Disponible en Windows Installer 4,0. |
| [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)                         | Consulta para obtener información acerca de la aplicación de una revisión especificada a un producto especificado. Disponible en Windows Installer 3,0.                                     |
| [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)               | Extrae información de una revisión. Disponible en Windows Installer 3,0.                                                                                             |
| [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) | Determina el mejor conjunto de revisiones necesarias para actualizar un producto o conjunto de productos. Disponible en Windows Installer 3,0.                                            |



 

## <a name="file-query-functions"></a>Funciones de consulta de archivo



| Nombre                                                                     | Descripción                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)                                 | Toma la ruta de acceso a un archivo y devuelve un hash de 128 bits de ese archivo.                                           |
| [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa) | Toma la ruta de acceso a un archivo que se ha firmado digitalmente y devuelve el certificado del firmante y el hash del archivo. |
| [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona)                           | Devuelve la cadena de versión y la cadena de idioma.                                                             |



 

## <a name="transaction-management-functions"></a>Funciones de administración de transacciones



| Nombre                                               | Descripción                                                                                                                                                                                         |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona) | Inicia el procesamiento de transacciones de una instalación de varios paquetes y devuelve un identificador para la transacción. Esta función está disponible a partir de Windows Installer 4,5.                    |
| [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)   | Solicita que el Windows Installer hacer que el proceso actual sea el propietario de la transacción que instala una instalación de varios paquetes. Esta función está disponible a partir de Windows Installer 4,5. |
| [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)     | Confirma o revierte todas las instalaciones que pertenecen a la transacción. Esta función está disponible a partir de Windows Installer 4,5.                                                          |



 

## <a name="database-functions"></a>Funciones de base de datos

Además de las funciones de Windows Installer identificadas en las tablas anteriores, puede manipular la información de la base de datos de instalación mediante las funciones de acceso a bases de datos que se describen en la sección [funciones de base de datos](database-functions.md) .

## <a name="installer-structures"></a>Estructuras de instalador

Además, parte de la información de la base de datos de instalación se controla mediante las estructuras descritas en la sección [estructuras del instalador](installer-structures.md) .

 

 




