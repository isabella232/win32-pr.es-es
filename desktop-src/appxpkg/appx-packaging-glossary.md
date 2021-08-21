---
title: Glosario de empaquetado, implementación y consulta
description: Proporciona definiciones de términos relacionados con el empaquetado, la implementación y la consulta de Windows aplicaciones.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a273b82806a724e50c7f29c512d19e1723283582abb3aa8b97f49f6293182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130277"
---
# <a name="packaging-deployment-and-query-glossary"></a>Glosario de empaquetado, implementación y consulta

<dl> <dt>

<span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**Id. de modelo de usuario de la aplicación**
</dt> <dd>

El identificador de modelo de usuario de la aplicación identifica de forma única una aplicación en el sistema operativo para que el sistema operativo pueda enviar notificaciones y así sucesivamente a la aplicación.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**mapa de bloques**
</dt> <dd>

Define los índices y los hashes criptográficos para los bloques de código ejecutable y los datos que se almacenan en los archivos de un paquete de aplicación. Se BlockMap.xml archivo para cada paquete de aplicación.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**paquete de dependencia**
</dt> <dd>

Paquete del que depende otro paquete. La dependencia se declara en el manifiesto del paquete dependiente y no en el manifiesto del paquete de dependencia.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**paquete dependiente**
</dt> <dd>

Un paquete que toma una dependencia de otro paquete. La dependencia se declara en el manifiesto del paquete dependiente.

</dd> <dt>

<span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**archivos de superficie**
</dt> <dd>

Archivos dentro de un paquete de aplicación que no forman parte de la aplicación que se va a implementar. Estos archivos proporcionan metadatos relacionados con el paquete. Los archivos de superficie estándar incluyen el manifiesto, el mapa de bloques, el mapa de flujo y la firma digital. Los archivos de superficie se crean como parte del proceso de compilación del paquete. Además, según la especificación de OPC, los tipos de.xml y los archivos cuyos nombres coinciden con el patrón \[ \_ \] \* \\ \_ \\ \* "rels .rels" son archivos de superficie.

</dd> <dt>

<span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**Manifiesto**
</dt> <dd>

Un archivo XML que describe el contenido y los metadatos asociados a un paquete, incluido el identificador del paquete. Se requiere un archivo XML de manifiesto para cada paquete de aplicación.

</dd> <dt>

<span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**Opc**
</dt> <dd>

Convenciones de empaquetado abierto (OPC) describe una tecnología de archivo de contenedor que se documenta en los estándares ISO/IEC 29500 y ECMA 376. Los paquetes de aplicaciones son compatibles con OPC.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**Paquete**
</dt> <dd>

Unidad de software de implementación, administración y mantenimiento asociada al modelo de empaquetado de aplicaciones. Un paquete contiene los archivos que constituyen la aplicación, junto con un archivo de manifiesto que describe el software que se va a Windows.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**nombre de familia del paquete**
</dt> <dd>

Forma serializada del identificador de paquete que representa de forma única la familia de paquetes en el equipo. Es adecuado para asignar nombres a objetos como archivos y carpetas. El nombre de familia del paquete es similar al nombre completo del paquete, pero solo incluye el nombre y el publicador. Dado que excluye la información que cambia con el mantenimiento (versión, arquitectura e información de recursos), resulta útil para las referencias independientes de la versión al paquete.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**nombre completo del paquete**
</dt> <dd>

Forma serializada del identificador de paquete que representa de forma única esta versión del paquete en el equipo. Es adecuado para asignar nombres a objetos como archivos y carpetas.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**id. de paquete**
</dt> <dd>

Identificador único global de un paquete. Se compone de una tupla de atributos para el paquete, incluidos el nombre, el publicador, la arquitectura admitida, la información de recursos y la versión. Consulte el nombre completo del paquete y el nombre de familia del paquete para obtener información sobre los formularios serializados del identificador de paquete.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**id. de aplicación relativa del paquete**
</dt> <dd>

Atributo **Id** del elemento [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) dentro del manifiesto del paquete, que también se conoce como PRAID. Esta cadena identifica de forma única una aplicación dentro de un paquete. Este atributo es necesario para el **elemento Application.**

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**archivos de carga**
</dt> <dd>

Los archivos de un paquete de aplicación que forman parte de la aplicación que se va a implementar. Estos archivos se extraen y colocan en la carpeta de instalación del usuario.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**id. de recurso**
</dt> <dd>

Parte opcional de un identificador de paquete que se usa para diferenciar los recursos del paquete. Por ejemplo, se puede usar un identificador de recurso para especificar el idioma o la configuración regional.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Directorio central de ZIP**
</dt> <dd>

Secuencias de bytes en un archivo ZIP que almacenan metadatos sobre el archivo ZIP y su contenido, incluidos el nombre, el tamaño, la configuración de compresión y la ubicación dentro del archivo.

</dd> </dl>

 

 