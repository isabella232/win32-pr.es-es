---
description: Se debe crear inicialmente un objeto instalador para cargar la compatibilidad de automatización necesaria para que COM tenga acceso a las funciones del instalador. Este objeto proporciona contenedores para crear los objetos de nivel superior y obtener acceso a sus métodos.
ms.assetid: fefc3e39-073e-4869-86b7-27d20a3b337b
title: Instalador (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4afddcce55a739ad322be10c736a6e9119f5c9eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653325"
---
# <a name="installer-object"></a>Instalador (objeto)

Se debe crear inicialmente un objeto **instalador** para cargar la compatibilidad de automatización necesaria para que com tenga acceso a las funciones del instalador. Este objeto proporciona contenedores para crear los objetos de nivel superior y obtener acceso a sus métodos.

Puede crear el objeto **instalador** desde el ProgID "WindowsInstaller. Installer".

## <a name="members"></a>Miembros

El objeto de **instalador** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **instalador** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                                                                     |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddSource**](installer-addsource.md)                                 | Agrega un origen a la lista de orígenes de red válidos en el SourceList.<br/>                                                                                                                |
| [**AdvertiseProduct**](installer-advertiseproduct.md)                   | Anuncia un paquete de instalación.<br/>                                                                                                                                                  |
| [**AdvertiseScript**](installer-advertisescript.md)                     | Anuncia un paquete de instalación. <br/>                                                                                                                                                 |
| [**ApplyMultiplePatches**](installer-applymultiplepatches.md)           | Aplica una o más revisiones a productos que puedan recibir la revisión. Establece la propiedad [**patch**](patch.md) en la ruta de acceso de los paquetes de revisión proporcionados.<br/>                          |
| [**ApplyPatch**](installer-applypatch.md)                               | Invoca una instalación de y establece la propiedad [**patch**](patch.md) en la ruta de acceso del paquete patch para cada producto incluido en el paquete patch como válido para recibir la revisión.<br/> |
| [**ClearSourceList**](installer-clearsourcelist.md)                     | Quita todos los orígenes de red de la SourceList.<br/>                                                                                                                                     |
| [**CollectUserInfo**](installer-collectuserinfo.md)                     | Invoca una secuencia del Asistente para interfaz de usuario que recopila y almacena la información de usuario y el código de producto.<br/>                                                                        |
| [**ConfigureFeature**](installer-configurefeature.md)                   | Configura el estado instalado de una característica del producto.<br/>                                                                                                                                 |
| [**ConfigureProduct**](installer-configureproduct.md)                   | Instala o desinstala un producto.<br/>                                                                                                                                                    |
| [**CreateAdvertiseScript**](installer-createadvertisescript.md)         | Genera un script de anuncio.<br/>                                                                                                                                                       |
| [**CreateRecord**](installer-createrecord.md)                           | Devuelve un nuevo objeto [**Record**](record-object.md) con el número de campos solicitado.<br/>                                                                                            |
| [**EnableLog**](installer-enablelog.md)                                 | Habilita el registro del tipo de mensaje seleccionado para todas las sesiones de instalación posteriores en el espacio de proceso actual.<br/>                                                                  |
| [**ExtractPatchXMLData**](installer-extractpatchxmldata.md)             | Extrae información de una revisión como una cadena XML.<br/>                                                                                                                                  |
| [**FileHash**](installer-filehash.md)                                   | Toma la ruta de acceso a un archivo y devuelve un hash de 128 bits de ese archivo.<br/>                                                                                                                    |
| [**FileSignatureInfo**](installer-filesignatureinfo.md)                 | Toma la ruta de acceso a un archivo y devuelve una **matriz SafeArray** de bytes que representa el hash o el certificado codificado.<br/>                                                                   |
| [**FileSize**](installer-filesize.md)                                   | Devuelve el tamaño del archivo especificado.<br/>                                                                                                                                              |
| [**FileVersion**](installer-fileversion.md)                             | Devuelve la cadena de versión o la cadena de idioma de la ruta de acceso especificada.<br/>                                                                                                                 |
| [**ForceSourceListResolution**](installer-forcesourcelistresolution.md) | Obliga al instalador a buscar en la lista de origen un origen de producto válido la próxima vez que se requiera un origen.<br/>                                                                        |
| [**InstallProduct**](installer-installproduct.md)                       | Abre un paquete del instalador e inicializa una sesión de instalación.<br/>                                                                                                                  |
| [**LastErrorRecord**](installer-lasterrorrecord.md)                     | Devuelve un objeto de [**registro**](record-object.md) que contiene los parámetros de error del error más reciente de la función que generó el registro de errores.<br/>                          |
| [**OpenDatabase**](installer-opendatabase.md)                           | Abre una base de datos existente o crea una nueva.<br/>                                                                                                                                     |
| [**OpenPackage**](installer-openpackage.md)                             | Abre un paquete del instalador para su uso con funciones que tienen acceso a la base de datos del producto e instalan el motor.<br/>                                                                               |
| [**OpenProduct**](installer-openproduct.md)                             | Abre un paquete del instalador para un producto instalado mediante el código de producto.<br/>                                                                                                          |
| [**ProvideAssembly**](installer-provideassembly.md)                     | Devuelve la ruta de acceso de instalación de un ensamblado.<br/>                                                                                                                                           |
| [**ProvideComponent**](installer-providecomponent.md)                   | Devuelve la ruta de acceso completa del componente y realiza cualquier instalación necesaria.<br/>                                                                                                             |
| [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) | Devuelve la ruta de acceso completa del componente y realiza cualquier instalación necesaria.<br/>                                                                                                             |
| [**Deleteinstance**](installer-registryvalue.md)                         | Lee información acerca de una clave del registro especificada de Value.<br/>                                                                                                                           |
| [**ReinstallFeature**](installer-reinstallfeature.md)                   | Vuelve a instalar características o corrige problemas con las características instaladas.<br/>                                                                                                                    |
| [**ReinstallProduct**](installer-reinstallproduct.md)                   | Vuelve a instalar un producto o corrige los problemas de instalación en un producto instalado.<br/>                                                                                                      |
| [**RemovePatches**](installer-removepatches.md)                         | Quita una o más revisiones de los productos que puedan recibir la revisión. <br/>                                                                                                              |
| [**UseFeature**](installer-usefeature.md)                               | Incrementa el recuento de uso de una característica determinada y devuelve el estado de instalación de esa característica.<br/>                                                                             |



 

### <a name="properties"></a>Propiedades

El objeto de **instalador** tiene estas propiedades.



| Propiedad                                                                    | Tipo de acceso           | Descripción                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientsEx**](installer-components.md)<br/>                        |                       | Devuelve un objeto [**RecordList**](recordlist-object.md) que muestra los productos que utilizan un componente instalado especificado.<br/> **[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** No compatible.<br/>       |
| [**ComponentClients**](installer-componentclients.md)<br/>           |                       | Devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de clientes de un componente especificado.<br/>                                                                                                                           |
| [**ComponentPath**](installer-componentpath.md)<br/>                 |                       | Devuelve la ruta de acceso completa a un componente instalado.<br/>                                                                                                                                                                                            |
| [**ComponentPathEx**](installer-componentpathex.md)<br/>             |                       | Devuelve un objeto [**RecordList**](recordlist-object.md) que proporciona la ruta de acceso completa de un componente instalado especificado. <br/> **[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** No compatible.<br/>       |
| [**ComponentQualifiers**](installer-componentqualifiers.md)<br/>     |                       | Devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de calificadores registrados para el componente especificado.<br/>                                                                                                          |
| [**Componentes**](installer-components.md)<br/>                       |                       | Devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de componentes instalados para todos los productos.<br/>                                                                                                                      |
| [**ComponentsEx**](installer-componentsex.md)<br/>                   |                       | Devuelve un objeto [**RecordList**](recordlist-object.md) que muestra los componentes instalados.<br/> **[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** No compatible.<br/>                                    |
| [**Entorno**](installer-environment.md)<br/>                     | Lectura/escritura<br/> | Valor de cadena para una variable de entorno del proceso actual.<br/>                                                                                                                                                                        |
| [**FeatureParent**](installer-featureparent.md)<br/>                 |                       | Especifica la característica primaria de una característica.<br/>                                                                                                                                                                                                  |
| [**Características**](installer-features.md)<br/>                           |                       | Devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de características publicadas para el producto especificado.<br/>                                                                                                               |
| [**FeatureState**](installer-featurestate.md)<br/>                   |                       | Devuelve el estado de instalación de una característica.<br/>                                                                                                                                                                                                   |
| [**FeatureUsageCount**](installer-featureusagecount.md)<br/>         |                       | Devuelve el número de veces que se ha utilizado la característica.<br/>                                                                                                                                                                                 |
| [**FeatureUsageDate**](installer-featureusagedate.md)<br/>           |                       | Devuelve la fecha en que se usó la característica especificada por última vez.<br/>                                                                                                                                                                                  |
| [**FileAttributes**](installer-fileattributes.md)<br/>               |                       | Devuelve un número que representa los atributos de archivo combinados para la ruta de acceso designada a un archivo o carpeta.<br/>                                                                                                                                  |
| [**Revisiones**](installer-patches.md)<br/>                             |                       | Devuelve un objeto [**StringList**](stringlist-object.md) que contiene todas las revisiones aplicadas al producto.<br/>                                                                                                                              |
| [**PatchesEx**](installer-patchesex.md)<br/>                         |                       | Enumera una colección de objetos [**patch**](patch-object.md) .<br/>                                                                                                                                                                           |
| [**PatchFiles**](installer-patchfiles.md)<br/>                       |                       | Devuelve un objeto [**StringList**](stringlist-object.md) que contiene una lista de archivos que se pueden actualizar mediante la lista de revisiones proporcionada.<br/>                                                                                                 |
| [**PatchInfo**](installer-patchinfo.md)<br/>                         |                       | Devuelve información acerca de una revisión.<br/>                                                                                                                                                                                                          |
| [**PatchTransforms**](installer-patchtransforms.md)<br/>             |                       | Devuelve la lista delimitada por punto y coma de las transformaciones que se encuentran en el paquete de revisión especificado y que se aplican al producto especificado.<br/>                                                                                                            |
| [**ProductElevated**](installer-productelevated.md)<br/>             |                       | Devuelve true si el producto está administrado o false si el producto no está administrado.<br/>                                                                                                                                                              |
| [**ProductInfo**](installer-productinfo.md)<br/>                     |                       | Devuelve el valor del atributo especificado para un producto instalado o publicado.<br/>                                                                                                                                                         |
| [**ProductInfoFromScript**](installer-productinfofromscript.md)<br/> |                       | Devuelve el valor del atributo especificado que se almacena en un script de anuncio.<br/>                                                                                                                                                         |
| [**Productos**](installer-products.md)<br/>                           |                       | Devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de todos los productos instalados o anunciados para el usuario y el equipo actuales. <br/>                                                                                     |
| [**ProductsEx**](installer-productsex.md)<br/>                       |                       | Enumera una colección de objetos [**Product**](product-object.md) .<br/>                                                                                                                                                                       |
| [**ProductState**](installer-productstate-property.md)<br/>          |                       | Devuelve la información de estado de instalación de un producto.<br/>                                                                                                                                                                                        |
| [**QualifierDescription**](installer-qualifierdescription.md)<br/>   |                       | Devuelve una cadena de texto que describe el componente calificado.<br/>                                                                                                                                                                               |
| [**Productosrelacionados**](installer-relatedproducts.md)<br/>             |                       | Devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de todos los productos instalados o anunciados para el usuario y el equipo actuales con una propiedad [**UpgradeCode**](upgradecode.md) especificada en su tabla de propiedades.<br/> |
| [**ShortcutTarget**](installer-shortcuttarget.md)<br/>               |                       | Examina un acceso directo y devuelve su producto, nombre de característica y componente si está disponible.<br/>                                                                                                                                                       |
| [**SummaryInformation**](installer-summaryinformation.md)<br/>       |                       | Devuelve un objeto [**SummaryInfo**](summaryinfo-object.md) que se puede utilizar para examinar, actualizar y agregar propiedades a la secuencia de información de Resumen de un paquete o transformación.<br/>                                                              |
| [**Elemento uilevel**](installer-uilevel.md)<br/>                             | Lectura/escritura<br/> | Indica el tipo de interfaz de usuario que se va a utilizar al abrir y procesar los paquetes posteriores en el espacio de proceso actual.<br/>                                                                                                           |
| [**Versión**](installer-version.md)<br/>                             |                       | Devuelve la representación de cadena de la versión actual de Windows Installer.<br/>                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar la interfaz de automatización](using-the-automation-interface.md)
</dt> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




