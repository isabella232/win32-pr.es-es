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
# <a name="packaging-deployment-and-query-glossary"></a><span data-ttu-id="f9c0c-103">Paquete, implementación y Glosario de consultas</span><span class="sxs-lookup"><span data-stu-id="f9c0c-103">Packaging, deployment, and query glossary</span></span>

<dl> <dt>

<span data-ttu-id="f9c0c-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**IDENTIFICADOR de modelo de usuario de aplicación**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**application user model ID**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-105">El identificador de modelo de usuario de la aplicación identifica de forma única una aplicación en el sistema operativo para que el sistema operativo pueda enviar notificaciones y así sucesivamente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-105">The application user model ID uniquely identifies an app on the operating system so the operating system can send notifications and so on to the app.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**asignación de bloques**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**block map**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-107">Define los índices y los hashes criptográficos para los bloques de código ejecutable y los datos que se almacenan en los archivos de un paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-107">Defines the indices and cryptographic hashes for blocks of executable code and data that are stored in the files of an app package.</span></span> <span data-ttu-id="f9c0c-108">Se requiere un archivo BlockMap.xml para cada paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-108">A BlockMap.xml file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**paquete de dependencia**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**dependency package**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-110">Paquete del que depende otro paquete.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-110">A package on which another package depends.</span></span> <span data-ttu-id="f9c0c-111">La dependencia se declara en el manifiesto del paquete dependiente y no en el manifiesto del paquete de dependencia.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-111">The dependency is declared in the dependent package's manifest and not in the dependency package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**paquete dependiente**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**dependent package**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-113">Paquete que toma una dependencia en otro paquete.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-113">A package that takes a dependency on another package.</span></span> <span data-ttu-id="f9c0c-114">La dependencia se declara en el manifiesto del paquete dependiente.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-114">The dependency is declared in the dependent package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**archivos de superficie**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**footprint files**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-116">Archivos dentro de un paquete de la aplicación que no forman parte de la aplicación que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-116">Files within an app package that are not part of the app to be deployed.</span></span> <span data-ttu-id="f9c0c-117">Estos archivos proporcionan metadatos que pertenecen al paquete.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-117">These files provide metadata pertaining to the package.</span></span> <span data-ttu-id="f9c0c-118">Los archivos de superficie estándar incluyen el manifiesto, el mapa de bloques, el mapa de flujo y la firma digital.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-118">Standard footprint files include the manifest, block map, stream map, and digital signature.</span></span> <span data-ttu-id="f9c0c-119">Los archivos de superficie se crean como parte del proceso de compilación del paquete.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-119">Footprint files are created as part of the package build process.</span></span> <span data-ttu-id="f9c0c-120">Además, según la especificación de OPC, los \[ tipos de contenido \_ \] . XML y los archivos cuyos nombres coinciden con el \* \\ \_ patrón "Rels \\ \* . Rels" son archivos de superficie.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-120">In addition per the OPC specification, \[Content\_Types\].xml and files whose names match the "\*\\\_rels\\\*.rels" pattern are footprint files.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifiesto**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifest**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-122">Archivo XML que describe el contenido y los metadatos asociados a un paquete, incluido el identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-122">An XML file that describes the contents and metadata associated with a package including the package ID.</span></span> <span data-ttu-id="f9c0c-123">Se requiere un archivo XML de manifiesto para cada paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-123">A manifest XML file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-125">Open Packaging Conventions (OPC) describe una tecnología de archivos de contenedor que se documenta en los estándares ISO/IEC 29500 y ECMA 376.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-125">Open Packaging Conventions (OPC) describes a container-file technology that is documented in the ISO/IEC 29500 and ECMA 376 standards.</span></span> <span data-ttu-id="f9c0c-126">Los paquetes de aplicaciones son compatibles con OPC.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-126">App packages are OPC-compliant.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**configura**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-128">Unidad de software de implementación, administración y mantenimiento asociada al modelo de empaquetado de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-128">The unit of deployment, management, and servicing software associated with the app packaging model.</span></span> <span data-ttu-id="f9c0c-129">Un paquete contiene los archivos que constituyen la aplicación, junto con un archivo de manifiesto que describe el software para Windows.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-129">A package contains the files that constitute the app, along with a manifest file that describes the software to Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**nombre de familia de paquete**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**package family name**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-131">Formato serializado del identificador de paquete que representa de forma única la familia de paquetes en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-131">A serialized form of the package ID that uniquely represents the package family on the computer.</span></span> <span data-ttu-id="f9c0c-132">Es adecuado para asignar nombres a objetos como archivos y carpetas.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-132">It is suitable for naming objects such as files and folders.</span></span> <span data-ttu-id="f9c0c-133">El nombre de familia del paquete es similar al nombre completo del paquete, pero solo incluye el nombre y el publicador.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-133">The package family name is similar to the package full name, but includes only the name and publisher.</span></span> <span data-ttu-id="f9c0c-134">Como excluye la información que cambia con el servicio (versión, arquitectura e información de recursos), resulta útil para las referencias independientes de la versión al paquete.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-134">Because it excludes info that changes with servicing (version, architecture, and resource info), it is useful for version-independent references to the package.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**nombre completo del paquete**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**package full name**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-136">Formato serializado del identificador de paquete que representa de forma única esta versión del paquete en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-136">A serialized form of the package ID that uniquely represents this version of the package on the computer.</span></span> <span data-ttu-id="f9c0c-137">Es adecuado para asignar nombres a objetos como archivos y carpetas.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-137">It is suitable for naming objects such as files and folders.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**IDENTIFICADOR de paquete**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**package ID**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-139">Un identificador único global para un paquete.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-139">A globally unique identifier for a package.</span></span> <span data-ttu-id="f9c0c-140">Se compone de una tupla de atributos para el paquete, incluidos el nombre, el publicador, la arquitectura admitida, la información de recursos y la versión.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-140">It is composed of a tuple of attributes for the package including name, publisher, supported architecture, resource info, and version.</span></span> <span data-ttu-id="f9c0c-141">Consulte nombre completo de paquete y nombre de familia de paquete para las formas serializadas del identificador de paquete.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-141">See package full name and package family name for serialized forms of the package ID.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**IDENTIFICADOR de aplicación relativa de paquete**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**package relative application ID**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-143">El atributo **ID** del elemento [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) en el manifiesto del paquete, que también se conoce como PRAID.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-143">The **Id** attribute on the [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) element within the package manifest, which is also known as PRAID.</span></span> <span data-ttu-id="f9c0c-144">Esta cadena identifica de forma única una aplicación dentro de un paquete.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-144">This string uniquely identifies an app within a package.</span></span> <span data-ttu-id="f9c0c-145">Este atributo es necesario para el elemento **Application** .</span><span class="sxs-lookup"><span data-stu-id="f9c0c-145">This attribute is required for the **Application** element.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**archivos de carga**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**payload files**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-147">Archivos de un paquete de la aplicación que forman parte de la aplicación que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-147">The files within an app package that are part of the app to be deployed.</span></span> <span data-ttu-id="f9c0c-148">Estos archivos se extraen y se colocan en la carpeta de instalación del usuario.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-148">These files are extracted and placed in the user's installation folder.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**IDENTIFICADOR de recurso**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**resource ID**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-150">Parte opcional de un identificador de paquete que se usa para diferenciar los recursos del paquete.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-150">An optional part of a package ID that is used to differentiate the resources in the package.</span></span> <span data-ttu-id="f9c0c-151">Por ejemplo, un identificador de recurso se puede usar para especificar el idioma o la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-151">For example, a resource ID can be used to specify the language or locale.</span></span>

</dd> <dt>

<span data-ttu-id="f9c0c-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Directorio central de ZIP**</span><span class="sxs-lookup"><span data-stu-id="f9c0c-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**ZIP central directory**</span></span>
</dt> <dd>

<span data-ttu-id="f9c0c-153">Secuencias de bytes en un archivo ZIP que almacenan metadatos sobre el archivo ZIP y su contenido, incluidos el nombre, el tamaño, la configuración de compresión y la ubicación dentro del archivo.</span><span class="sxs-lookup"><span data-stu-id="f9c0c-153">The byte sequences in a ZIP file that store metadata about the ZIP archive and its contents including name, size, compression settings, and location within the archive.</span></span>

</dd> </dl>

 

 