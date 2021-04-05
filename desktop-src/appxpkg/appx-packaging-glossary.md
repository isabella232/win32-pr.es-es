---
title: Paquete, implementación y Glosario de consultas
description: Proporciona definiciones de los términos relacionados con el empaquetado, la implementación y la consulta de aplicaciones de Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2112b593e2d2a5aaf4f06525160e2d799bad1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104420532"
---
# <a name="packaging-deployment-and-query-glossary"></a>Paquete, implementación y Glosario de consultas

<dl> <dt>

<span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**IDENTIFICADOR de modelo de usuario de aplicación**
</dt> <dd>

El identificador de modelo de usuario de la aplicación identifica de forma única una aplicación en el sistema operativo para que el sistema operativo pueda enviar notificaciones y así sucesivamente a la aplicación.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**asignación de bloques**
</dt> <dd>

Define los índices y los hashes criptográficos para los bloques de código ejecutable y los datos que se almacenan en los archivos de un paquete de la aplicación. Se requiere un archivo BlockMap.xml para cada paquete de la aplicación.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**paquete de dependencia**
</dt> <dd>

Paquete del que depende otro paquete. La dependencia se declara en el manifiesto del paquete dependiente y no en el manifiesto del paquete de dependencia.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**paquete dependiente**
</dt> <dd>

Paquete que toma una dependencia en otro paquete. La dependencia se declara en el manifiesto del paquete dependiente.

</dd> <dt>

<span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**archivos de superficie**
</dt> <dd>

Archivos dentro de un paquete de la aplicación que no forman parte de la aplicación que se va a implementar. Estos archivos proporcionan metadatos que pertenecen al paquete. Los archivos de superficie estándar incluyen el manifiesto, el mapa de bloques, el mapa de flujo y la firma digital. Los archivos de superficie se crean como parte del proceso de compilación del paquete. Además, según la especificación de OPC, los \[ tipos de contenido \_ \] . XML y los archivos cuyos nombres coinciden con el \* \\ \_ patrón "Rels \\ \* . Rels" son archivos de superficie.

</dd> <dt>

<span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifiesto**
</dt> <dd>

Archivo XML que describe el contenido y los metadatos asociados a un paquete, incluido el identificador del paquete. Se requiere un archivo XML de manifiesto para cada paquete de aplicación.

</dd> <dt>

<span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**
</dt> <dd>

Open Packaging Conventions (OPC) describe una tecnología de archivos de contenedor que se documenta en los estándares ISO/IEC 29500 y ECMA 376. Los paquetes de aplicaciones son compatibles con OPC.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**configura**
</dt> <dd>

Unidad de software de implementación, administración y mantenimiento asociada al modelo de empaquetado de aplicaciones. Un paquete contiene los archivos que constituyen la aplicación, junto con un archivo de manifiesto que describe el software para Windows.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**nombre de familia de paquete**
</dt> <dd>

Formato serializado del identificador de paquete que representa de forma única la familia de paquetes en el equipo. Es adecuado para asignar nombres a objetos como archivos y carpetas. El nombre de familia del paquete es similar al nombre completo del paquete, pero solo incluye el nombre y el publicador. Como excluye la información que cambia con el servicio (versión, arquitectura e información de recursos), resulta útil para las referencias independientes de la versión al paquete.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**nombre completo del paquete**
</dt> <dd>

Formato serializado del identificador de paquete que representa de forma única esta versión del paquete en el equipo. Es adecuado para asignar nombres a objetos como archivos y carpetas.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**IDENTIFICADOR de paquete**
</dt> <dd>

Un identificador único global para un paquete. Se compone de una tupla de atributos para el paquete, incluidos el nombre, el publicador, la arquitectura admitida, la información de recursos y la versión. Consulte nombre completo de paquete y nombre de familia de paquete para las formas serializadas del identificador de paquete.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**IDENTIFICADOR de aplicación relativa de paquete**
</dt> <dd>

El atributo **ID** del elemento [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) en el manifiesto del paquete, que también se conoce como PRAID. Esta cadena identifica de forma única una aplicación dentro de un paquete. Este atributo es necesario para el elemento **Application** .

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**archivos de carga**
</dt> <dd>

Archivos de un paquete de la aplicación que forman parte de la aplicación que se va a implementar. Estos archivos se extraen y se colocan en la carpeta de instalación del usuario.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**IDENTIFICADOR de recurso**
</dt> <dd>

Parte opcional de un identificador de paquete que se usa para diferenciar los recursos del paquete. Por ejemplo, un identificador de recurso se puede usar para especificar el idioma o la configuración regional.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Directorio central de ZIP**
</dt> <dd>

Secuencias de bytes en un archivo ZIP que almacenan metadatos sobre el archivo ZIP y su contenido, incluidos el nombre, el tamaño, la configuración de compresión y la ubicación dentro del archivo.

</dd> </dl>

 

 