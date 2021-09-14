---
description: Se debe crear inicialmente un objeto Installer para cargar la compatibilidad de automatización necesaria para que COM acceda a las funciones del instalador. Este objeto proporciona contenedores para crear los objetos de nivel superior y acceder a sus métodos.
ms.assetid: fefc3e39-073e-4869-86b7-27d20a3b337b
title: Objeto del instalador
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072140"
---
# <a name="installer-object"></a>Objeto del instalador

Se **debe** crear inicialmente un objeto Installer para cargar la compatibilidad de automatización necesaria para que COM acceda a las funciones del instalador. Este objeto proporciona contenedores para crear los objetos de nivel superior y acceder a sus métodos.

Puede crear el objeto **Installer** desde el ProgId "WindowsInstaller.Installer".

## <a name="members"></a>Members

El **objeto** Installer tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Installer** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                                                                     |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddSource**](installer-addsource.md)                                 | Agrega un origen a la lista de orígenes de red válidos en la lista de orígenes.<br/>                                                                                                                |
| [**AdvertiseProduct**](installer-advertiseproduct.md)                   | Anuncia un paquete de instalación.<br/>                                                                                                                                                  |
| [**AdvertiseScript**](installer-advertisescript.md)                     | Anuncia un paquete de instalación. <br/>                                                                                                                                                 |
| [**ApplyMultiplePatches**](installer-applymultiplepatches.md)           | Aplica una o varias revisiones a los productos aptos para recibir la revisión. Establece la [**propiedad PATCH**](patch.md) en la ruta de acceso de los paquetes de revisión proporcionados.<br/>                          |
| [**ApplyPatch**](installer-applypatch.md)                               | Invoca una instalación y establece la propiedad [**PATCH**](patch.md) en la ruta de acceso del paquete de revisión para cada producto enumerado por el paquete de revisión como apto para recibir la revisión.<br/> |
| [**ClearSourceList**](installer-clearsourcelist.md)                     | Quita todos los orígenes de red de la lista de orígenes.<br/>                                                                                                                                     |
| [**CollectUserInfo**](installer-collectuserinfo.md)                     | Invoca una secuencia del asistente de interfaz de usuario que recopila y almacena la información de usuario y el código de producto.<br/>                                                                        |
| [**ConfigureFeature**](installer-configurefeature.md)                   | Configura el estado instalado de una característica de producto.<br/>                                                                                                                                 |
| [**ConfigureProduct**](installer-configureproduct.md)                   | Instala o desinstala un producto.<br/>                                                                                                                                                    |
| [**CreateAdvertiseScript**](installer-createadvertisescript.md)         | Genera un script de anuncio.<br/>                                                                                                                                                       |
| [**CreateRecord**](installer-createrecord.md)                           | Devuelve un nuevo [**objeto Record**](record-object.md) con el número solicitado de campos.<br/>                                                                                            |
| [**EnableLog**](installer-enablelog.md)                                 | Habilita el registro del tipo de mensaje seleccionado para todas las sesiones de instalación posteriores en el espacio de proceso actual.<br/>                                                                  |
| [**ExtractPatchXMLData**](installer-extractpatchxmldata.md)             | Extrae información de una revisión como una cadena XML.<br/>                                                                                                                                  |
| [**FileHash**](installer-filehash.md)                                   | Toma la ruta de acceso a un archivo y devuelve un hash de 128 bits de ese archivo.<br/>                                                                                                                    |
| [**FileSignatureInfo**](installer-filesignatureinfo.md)                 | Toma la ruta de acceso a un archivo y devuelve **una SAFEARRAY** de bytes que representa el hash o el certificado codificado.<br/>                                                                   |
| [**FileSize**](installer-filesize.md)                                   | Devuelve el tamaño del archivo especificado.<br/>                                                                                                                                              |
| [**FileVersion**](installer-fileversion.md)                             | Devuelve la cadena de versión o la cadena de idioma de la ruta de acceso especificada.<br/>                                                                                                                 |
| [**ForceSourceListResolution**](installer-forcesourcelistresolution.md) | Obliga al instalador a buscar en la lista de origen un origen de producto válido la próxima vez que se requiera un origen.<br/>                                                                        |
| [**InstallProduct**](installer-installproduct.md)                       | Abre un paquete del instalador e inicializa una sesión de instalación.<br/>                                                                                                                  |
| [**LastErrorRecord**](installer-lasterrorrecord.md)                     | Devuelve un [**objeto Record**](record-object.md) que contiene parámetros de error para el error más reciente de la función que produjo el registro de errores.<br/>                          |
| [**OpenDatabase**](installer-opendatabase.md)                           | Abre una base de datos existente o crea una nueva.<br/>                                                                                                                                     |
| [**OpenPackage**](installer-openpackage.md)                             | Abre un paquete del instalador para usarlo con funciones que tienen acceso a la base de datos del producto y al motor de instalación.<br/>                                                                               |
| [**OpenProduct**](installer-openproduct.md)                             | Abre un paquete del instalador para un producto instalado mediante el código del producto.<br/>                                                                                                          |
| [**ProvideAssembly**](installer-provideassembly.md)                     | Devuelve la ruta de acceso instalada de un ensamblado.<br/>                                                                                                                                           |
| [**ProvideComponent**](installer-providecomponent.md)                   | Devuelve la ruta de acceso completa del componente y realiza cualquier instalación necesaria.<br/>                                                                                                             |
| [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) | Devuelve la ruta de acceso completa del componente y realiza cualquier instalación necesaria.<br/>                                                                                                             |
| [**RegistryValue**](installer-registryvalue.md)                         | Lee información sobre una clave de valor del Registro especificada.<br/>                                                                                                                           |
| [**ReinstallFeature**](installer-reinstallfeature.md)                   | Reinstala las características o corrige los problemas con las características instaladas.<br/>                                                                                                                    |
| [**ReinstallProduct**](installer-reinstallproduct.md)                   | Vuelve a instalar un producto o corrige los problemas de instalación en un producto instalado.<br/>                                                                                                      |
| [**RemovePatches**](installer-removepatches.md)                         | Quita una o varias revisiones a los productos aptos para recibir la revisión. <br/>                                                                                                              |
| [**UseFeature**](installer-usefeature.md)                               | Incrementa el recuento de uso de una característica determinada y devuelve el estado de instalación de esa característica.<br/>                                                                             |



 

### <a name="properties"></a>Propiedades

El **objeto Installer** tiene estas propiedades.



| Propiedad.                                                                    | Tipo de acceso           | Descripción                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientsEx**](installer-components.md)<br/>                        |                       | Devuelve un [**objeto RecordList**](recordlist-object.md) que enumera los productos que usan un componente instalado especificado.<br/> **[Windows Installer 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/>       |
| [**ComponentClients**](installer-componentclients.md)<br/>           |                       | Devuelve un [**objeto StringList**](stringlist-object.md) que enumera el conjunto de clientes de un componente especificado.<br/>                                                                                                                           |
| [**ComponentPath**](installer-componentpath.md)<br/>                 |                       | Devuelve la ruta de acceso completa a un componente instalado.<br/>                                                                                                                                                                                            |
| [**ComponentPathEx**](installer-componentpathex.md)<br/>             |                       | Devuelve un [**objeto RecordList**](recordlist-object.md) que proporciona la ruta de acceso completa de un componente instalado especificado. <br/> **[Windows Installer 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/>       |
| [**ComponentQualifiers**](installer-componentqualifiers.md)<br/>     |                       | Devuelve un [**objeto StringList**](stringlist-object.md) que enumera el conjunto de calificadores registrados para el componente especificado.<br/>                                                                                                          |
| [**Componentes**](installer-components.md)<br/>                       |                       | Devuelve un [**objeto StringList**](stringlist-object.md) que enumera el conjunto de componentes instalados para todos los productos.<br/>                                                                                                                      |
| [**ComponentesEx**](installer-componentsex.md)<br/>                   |                       | Devuelve un [**objeto RecordList**](recordlist-object.md) que enumera los componentes instalados.<br/> **[Windows Installer 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/>                                    |
| [**Ambiente**](installer-environment.md)<br/>                     | Lectura y escritura<br/> | Valor de cadena de una variable de entorno del proceso actual.<br/>                                                                                                                                                                        |
| [**FeatureParent**](installer-featureparent.md)<br/>                 |                       | Especifica la característica primaria de una característica.<br/>                                                                                                                                                                                                  |
| [**Características**](installer-features.md)<br/>                           |                       | Devuelve un [**objeto StringList**](stringlist-object.md) que enumera el conjunto de características publicadas para el producto especificado.<br/>                                                                                                               |
| [**FeatureState**](installer-featurestate.md)<br/>                   |                       | Devuelve el estado instalado de una característica.<br/>                                                                                                                                                                                                   |
| [**FeatureUsageCount**](installer-featureusagecount.md)<br/>         |                       | Devuelve el número de veces que se ha usado la característica.<br/>                                                                                                                                                                                 |
| [**FeatureUsageDate**](installer-featureusagedate.md)<br/>           |                       | Devuelve la fecha en que se usó por última vez la característica especificada.<br/>                                                                                                                                                                                  |
| [**FileAttributes**](installer-fileattributes.md)<br/>               |                       | Devuelve un número que representa los atributos de archivo combinados para la ruta de acceso designada a un archivo o carpeta.<br/>                                                                                                                                  |
| [**Parches**](installer-patches.md)<br/>                             |                       | Devuelve un [**objeto StringList**](stringlist-object.md) que contiene todas las revisiones aplicadas al producto.<br/>                                                                                                                              |
| [**PatchesEx**](installer-patchesex.md)<br/>                         |                       | Enumera una colección de objetos [**Patch.**](patch-object.md)<br/>                                                                                                                                                                           |
| [**PatchFiles**](installer-patchfiles.md)<br/>                       |                       | Devuelve un [**objeto StringList**](stringlist-object.md) que contiene una lista de archivos que se pueden actualizar mediante la lista de revisiones proporcionada.<br/>                                                                                                 |
| [**PatchInfo**](installer-patchinfo.md)<br/>                         |                       | Devuelve información sobre una revisión.<br/>                                                                                                                                                                                                          |
| [**PatchTransforms**](installer-patchtransforms.md)<br/>             |                       | Devuelve la lista delimitada por punto y coma de las transformaciones que se encuentran en el paquete de revisión especificado y que se aplican al producto especificado.<br/>                                                                                                            |
| [**ProductElevated**](installer-productelevated.md)<br/>             |                       | Devuelve True si el producto está administrado o False si el producto no está administrado.<br/>                                                                                                                                                              |
| [**ProductInfo**](installer-productinfo.md)<br/>                     |                       | Devuelve el valor del atributo especificado para un producto instalado o publicado.<br/>                                                                                                                                                         |
| [**ProductInfoFromScript**](installer-productinfofromscript.md)<br/> |                       | Devuelve el valor del atributo especificado que se almacena en un script de anuncio.<br/>                                                                                                                                                         |
| [**Productos**](installer-products.md)<br/>                           |                       | Devuelve un [**objeto StringList**](stringlist-object.md) que enumera el conjunto de todos los productos instalados o anunciados para el usuario y la máquina actuales. <br/>                                                                                     |
| [**ProductsEx**](installer-productsex.md)<br/>                       |                       | Enumera una colección de objetos [**Product.**](product-object.md)<br/>                                                                                                                                                                       |
| [**ProductState**](installer-productstate-property.md)<br/>          |                       | Devuelve la información de estado de instalación de un producto.<br/>                                                                                                                                                                                        |
| [**QualifierDescription**](installer-qualifierdescription.md)<br/>   |                       | Devuelve una cadena de texto que describe el componente completo.<br/>                                                                                                                                                                               |
| [**RelatedProducts**](installer-relatedproducts.md)<br/>             |                       | Devuelve un [**objeto StringList**](stringlist-object.md) que enumera el conjunto de todos los productos instalados o anunciados para el usuario y la máquina actuales con una propiedad [**UpgradeCode**](upgradecode.md) especificada en su tabla de propiedades.<br/> |
| [**ShortcutTarget**](installer-shortcuttarget.md)<br/>               |                       | Examina un acceso directo y devuelve su producto, nombre de característica y componente si está disponible.<br/>                                                                                                                                                       |
| [**SummaryInformation**](installer-summaryinformation.md)<br/>       |                       | Devuelve un [**objeto SummaryInfo**](summaryinfo-object.md) que se puede usar para examinar, actualizar y agregar propiedades al flujo de información de resumen de un paquete o transformación.<br/>                                                              |
| [**UILevel**](installer-uilevel.md)<br/>                             | Lectura y escritura<br/> | Indica el tipo de interfaz de usuario que se va a usar al abrir y procesar paquetes posteriores dentro del espacio de proceso actual.<br/>                                                                                                           |
| [**Versión**](installer-version.md)<br/>                             |                       | Devuelve la representación de cadena de la versión actual de Windows Installer.<br/>                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de la interfaz de Automation](using-the-automation-interface.md)
</dt> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




