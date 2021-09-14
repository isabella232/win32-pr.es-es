---
description: Para habilitar Windows Installer en la aplicación, debe usar las funciones del instalador. Las tablas de este tema identifican las funciones por categoría.
ms.assetid: 05a16915-6b47-4d51-b62a-5a4d92b87e50
title: Referencia de función del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9261789f21bd559e49c4e5718ef68ce9d0bb41c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072142"
---
# <a name="installer-function-reference"></a>Referencia de función del instalador

Para habilitar Windows Installer en la aplicación, debe usar las funciones del instalador. Las tablas de este tema identifican las funciones por categoría.

## <a name="user-interface-and-logging-functions"></a>Interfaz de usuario y funciones de registro



| Nombre                                                     | Descripción                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)             | Habilita la interfaz de usuario interna del instalador.                                 |
| [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)             | Habilita un controlador de interfaz de usuario externo que recibe mensajes en formato de cadena. |
| [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) | Habilita un controlador de interfaz de usuario externo que recibe mensajes en formato de registro. |
| [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)                     | Establece el modo de registro para todas las instalaciones del proceso de llamada.                       |



 

## <a name="handle-management-functions"></a>Controlar funciones de administración



| Nombre                                             | Descripción                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)         | Cierra un identificador de instalación abierto.                           |
| [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) | Cierra todos los identificadores de instalación abiertos. No use para la limpieza. |



 

## <a name="installation-and-configuration-functions"></a>Funciones de instalación y configuración



| Nombre                                                                     | Descripción                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)                       | Anuncia un producto.                                                                                                                                                                                                        |
| [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)                   | Anuncia un producto.                                                                                                                                                                                                        |
| [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)                         | Copia un archivo de script de anuncio en ubicaciones especificadas.                                                                                                                                                                    |
| [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)                           | Instala o quita una aplicación o un conjunto de aplicaciones.                                                                                                                                                                     |
| [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)                       | Instala o quita una aplicación o un conjunto de aplicaciones.                                                                                                                                                                     |
| [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)                   | Instala o quita una aplicación o un conjunto de aplicaciones. Se puede especificar una línea de comandos del producto.                                                                                                                            |
| [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)                       | Reinstala o repara una instalación.                                                                                                                                                                                       |
| [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)                       | Configura el estado instalado de una característica.                                                                                                                                                                                 |
| [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)                       | Valida o repara características.                                                                                                                                                                                               |
| [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)         | Instala los componentes que faltan.                                                                                                                                                                                                 |
| [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)                   | Instala los archivos que faltan.                                                                                                                                                                                                      |
| [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)                         | Notifica y actualiza la información interna Windows Installer con cambios en los SID de usuario. Disponible a partir Windows Installer 3.1.                                                                                   |
| [**MsiProcessAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiprocessadvertisescripta)           | Procesa un archivo de script de anuncio en ubicaciones especificadas.                                                                                                                                                                 |
| [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)                 | Agrega o reordena los orígenes de una revisión o un producto en un contexto especificado.                                                                                                                                                   |
| [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)             | Agrega o reordena los orígenes de una revisión o un producto en un contexto especificado. Crea una lista de origen para una revisión que no existe en un contexto especificado. Disponible en Windows Installer 3.0.                                |
| [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)             | Quita un origen existente para un producto o revisión en un contexto especificado. Disponible en Windows Installer 3.0.                                                                                                               |
| [**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)                   | Quita todos los orígenes existentes de un tipo de origen específico para una instancia de producto especificada.                                                                                                                                 |
| [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)               | Quita todos los orígenes existentes de un tipo de origen específico para una instancia de producto especificada. Disponible en Windows Installer 3.0.                                                                                            |
| [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)     | Quita el registro del origen actual del producto o la revisión, que se registra como la propiedad "LastUsedSource". Esta función no afecta a la lista de orígenes registrados.                                      |
| [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) | Quita el registro del origen actual del producto o la revisión, que se registra como la propiedad "LastUsedSource". Esta función no afecta a la lista de orígenes registrados. Disponible en Windows Installer 3.0. |
| [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)                     | Recupera información sobre la lista de origen de un producto o revisión en un contexto específico.                                                                                                                                    |
| [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)                     | Establece el origen usado más recientemente para un producto o revisión en un contexto especificado. Disponible en Windows Installer 3.0.                                                                                                       |
| [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)       | Enumera la lista de discos registrados para el origen multimedia de una revisión o un producto. Disponible en Windows Installer 3.0.                                                                                                    |
| [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)           | Agrega o actualiza un disco del origen multimedia de un producto o revisión registrado. Disponible en Windows Installer 3.0.                                                                                                            |
| [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)      | Quita un disco registrado existente en el origen multimedia de un producto o revisión en un contexto específico. Disponible en Windows Installer 3.0.                                                                                |
| [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)             | Enumera los orígenes en la lista de origen de un producto o revisión especificados. Disponible en Windows Installer 3.0.                                                                                                              |



 

## <a name="component-specific-functions"></a>Component-Specific Functions



| Nombre                                                                     | Descripción                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)                         | Instala y devuelve la ruta de acceso completa del componente para un ensamblado.                                                                                                                                                                 |
| [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)                       | Instala y devuelve la ruta de acceso completa del componente de un componente.                                                                                                                                                                  |
| [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)     | Instala y devuelve la ruta de acceso completa del componente de un componente calificado.                                                                                                                                                        |
| [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) | Instala y devuelve la ruta de acceso completa del componente de un componente calificado publicado por un producto.                                                                                                                         |
| [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)                       | Devuelve la ruta de acceso completa o la clave del Registro a un componente instalado.                                                                                                                                                              |
| [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)                   | Devuelve la ruta de acceso completa o la clave del Registro a un componente instalado entre cuentas de usuario y contexto de instalación. **[Windows instalador 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/> |
| [**MsiLocateComponent**](/windows/desktop/api/Msi/nf-msi-msilocatecomponenta)                         | Devuelve la ruta de acceso completa a un componente instalado sin un código de producto.                                                                                                                                                       |
| [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)                 | Devuelve el estado instalado de un componente. Puede consultar los componentes de una instancia de un producto instalado en cuentas de usuario que no son del usuario actual. Disponible en Windows Installer 3.0 o posterior.                        |



 

## <a name="application-only-functions"></a>Application-Only Functions



| Nombre                                             | Descripción                                                            |
|--------------------------------------------------|------------------------------------------------------------------------|
| [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) | Almacena información de usuario de un Asistente para instalación.                   |
| [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)           | Incrementa el recuento de uso de una característica e indica el estado de instalación. |
| [**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)       | Incrementa el recuento de uso de una característica e indica el estado de instalación. |
| [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)   | Devuelve código de producto mediante el código de componente.                         |



 

## <a name="system-status-functions"></a>Funciones de estado del sistema



| Nombre                                                             | Descripción                                                                                                                                                                                                                       |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)                       | Enumera los productos anunciados.                                                                                                                                                                                                   |
| [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)                   | Enumera todas las instancias de productos anunciados o instalados en un contexto especificado. Disponible en Windows Installer 3.0 o posterior.                                                                                    |
| [**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)         | Enumera los productos instalados actualmente que tienen un código de actualización especificado.                                                                                                                                                          |
| [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)                       | Enumera las características publicadas.                                                                                                                                                                                                    |
| [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)                   | Enumera los componentes instalados.                                                                                                                                                                                              |
| [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)               | Enumera los componentes instalados entre cuentas de usuario y contexto de instalación. **[Windows instalador 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/>                                 |
| [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)                         | Enumera los clientes de un componente instalado.                                                                                                                                                                                 |
| [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)                     | Enumera los clientes de un componente instalado entre las cuentas de usuario y el contexto de instalación. **[Windows instalador 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/>                    |
| [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) | Enumera los calificadores anunciados para un componente.                                                                                                                                                                             |
| [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)             | Devuelve el estado instalado de una característica.                                                                                                                                                                                         |
| [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)         | Devuelve el estado instalado de una característica de producto. Puede consultar características de una instancia de un producto instalado en cuentas de usuario que no son del usuario actual. Disponible en Windows Installer 3.0 o posterior.                        |
| [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)             | Devuelve el estado instalado para una aplicación o un conjunto de aplicaciones.                                                                                                                                                              |
| [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)                 | Devuelve las métricas de uso de una característica.                                                                                                                                                                                              |
| [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)                   | Devuelve información del producto para los productos publicados e instalados.                                                                                                                                                                 |
| [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)               | Devuelve información del producto para los productos anunciados e instalados. Puede recuperar información sobre una instancia de un producto instalado en una cuenta de usuario que no sea el usuario actual. Disponible en Windows Installer 3.0 o posterior. |
| [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)                         | Devuelve información de usuario registrada para un producto instalado.                                                                                                                                                                     |



 

## <a name="product-query-functions"></a>Funciones de consulta de producto



| Nombre                                                               | Descripción                                                                            |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)                           | Abre un producto para usarlo con las funciones que tienen acceso a la base de datos.                    |
| [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)                           | Abre un paquete para usarlo con las funciones que acceden a la base de datos.                    |
| [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)                       | Abre un paquete para usarlo con las funciones que acceden a la base de datos.                    |
| [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)               | Comprueba si el producto está instalado con privilegios elevados.                      |
| [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) | Devuelve información del producto para un archivo de script del instalador.                              |
| [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)             | Recupera las propiedades de la base de datos del producto.                                          |
| [**MsiGetShortcutTarget**](/windows/desktop/api/Msi/nf-msi-msigetshortcuttargeta)               | Examina un acceso directo y devuelve su producto, nombre de característica y componente si está disponible. |
| [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)                     | Devuelve información descriptiva para una característica.                                         |
| [**MsiVerifyPackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)                       | Comprueba que un archivo especificado es un paquete de instalación.                             |



 

## <a name="patching-functions"></a>Funciones de aplicación de revisiones



| Nombre                                                                   | Descripción                                                                                                                                                        |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)                                 | Invoca una instalación y aplica un paquete de revisión.                                                                                                               |
| [**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)                    | Devuelve el GUID de cada revisión que se aplica a un producto y una lista de transformaciones de cada revisión que se aplican al producto.                                  |
| [**MsiGetPatchInfo**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoa)                             | Devuelve información sobre una revisión.                                                                                                                                 |
| [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)                           | Desinstala una revisión de un producto. Disponible en Windows Installer 3.0.                                                                                             |
| [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)         | Determina la mejor secuencia de aplicación para un conjunto de revisiones y productos. Disponible en Windows Installer 3.0.                                                     |
| [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)             | Aplica una o varias revisiones a los productos. Disponible en Windows Installer 3.0.                                                                                       |
| [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)                           | Enumera todas las revisiones aplicadas a un producto en un contexto determinado o en todos los contextos. Disponible en Windows Installer 3.0.                                   |
| [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)                     | Cuando se proporciona una lista de archivos .msp, esta función recupera la lista de archivos que las revisiones pueden actualizar para la targe. Disponible en Windows Installer 4.0. |
| [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)                         | Consulta para obtener información sobre la aplicación de una revisión especificada a un producto especificado. Disponible en Windows Installer 3.0.                                     |
| [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)               | Extrae información de una revisión. Disponible en Windows Installer 3.0.                                                                                             |
| [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) | Determina el mejor conjunto de revisiones necesarias para actualizar un producto o un conjunto de productos. Disponible en Windows Installer 3.0.                                            |



 

## <a name="file-query-functions"></a>Funciones de consulta de archivos



| Nombre                                                                     | Descripción                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)                                 | Toma la ruta de acceso a un archivo y devuelve un hash de 128 bits de ese archivo.                                           |
| [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa) | Toma la ruta de acceso a un archivo que se ha firmado digitalmente y devuelve el certificado de firmante y el hash del archivo. |
| [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona)                           | Devuelve la cadena de versión y la cadena de idioma.                                                             |



 

## <a name="transaction-management-functions"></a>Funciones de administración de transacciones



| Nombre                                               | Descripción                                                                                                                                                                                         |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona) | Inicia el procesamiento de transacciones de una instalación de varios paquetes y devuelve un identificador para la transacción. Esta función está disponible a partir de Windows Installer 4.5.                    |
| [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)   | Solicita que el instalador Windows que el proceso actual sea el propietario de la transacción que instala una instalación de varios paquetes. Esta función está disponible a partir de Windows Installer 4.5. |
| [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)     | Confirma o revierte todas las instalaciones que pertenecen a la transacción. Esta función está disponible a partir de Windows Installer 4.5.                                                          |



 

## <a name="database-functions"></a>Funciones de base de datos

Además de las funciones Windows Installer identificadas en las tablas anteriores, puede manipular la información de la base de datos de instalación mediante las funciones de acceso a la base de datos que se describen en la sección Funciones de base de [datos.](database-functions.md)

## <a name="installer-structures"></a>Estructuras del instalador

Además, parte de la información de la base de datos de instalación se controla mediante las estructuras descritas en la sección [Estructuras del](installer-structures.md) instalador.

 

 




