---
title: API de consulta de paquetes
description: Obtenga información sobre la API de consulta de paquetes, que puede usar para obtener información sobre los paquetes de aplicación instalados en el sistema. Cada paquete de aplicación contiene los archivos que componen una aplicación de Windows y un archivo de manifiesto que describe el software para Windows.
ms.assetid: EDDFC8B1-E224-4921-BED6-FC81711BA5BF
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 5632edf661b4ea82177473bbb35f2674674500c6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077577"
---
# <a name="package-query-api"></a>API de consulta de paquetes

Obtenga información sobre la API de consulta de paquetes, que puede usar para obtener información sobre los paquetes de aplicación instalados en el sistema. Cada paquete de aplicación contiene los archivos que componen una aplicación de Windows y un archivo de manifiesto que describe el software para Windows.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                 | Descripción                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosePackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-closepackageinfo)<br/>                                               | Cierra una referencia a la información de paquete especificada.<br/>                                                                                              |
| [**FindPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-findpackagesbypackagefamily)<br/>                         | Busca los paquetes con el nombre de familia especificado para el usuario actual. <br/>                                                                              |
| [**FormatApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-formatapplicationusermodelid)<br/>                       | Construye un [identificador de modelo de usuario](appx-packaging-glossary.md) de la aplicación a partir del nombre de familia del paquete y del identificador de la aplicación relativa del paquete (PRAID). <br/> |
| [**GetApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelid)<br/>                             | Obtiene el [identificador del modelo de usuario](appx-packaging-glossary.md) de la aplicación para el proceso especificado.<br/>                                                          |
| [**GetApplicationUserModelIdFromToken**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelidfromtoken)<br/>           | Obtiene el [identificador de modelo de usuario](appx-packaging-glossary.md) de la aplicación para el token especificado.<br/>                                                            |
| [**GetCurrentApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getcurrentapplicationusermodelid)<br/>               | Obtiene el [identificador del modelo de usuario](appx-packaging-glossary.md) de la aplicación para el proceso actual.<br/>                                                            |
| [**GetCurrentPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefamilyname)<br/>                         | Obtiene el nombre de familia del paquete para el proceso que realiza la llamada.<br/>                                                                                                 |
| [**GetCurrentPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefullname)<br/>                             | Obtiene el nombre completo del paquete para el proceso que realiza la llamada.<br/>                                                                                                   |
| [**GetCurrentPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageid)<br/>                                         | Obtiene el identificador de paquete (ID.) del proceso que realiza la llamada.<br/>                                                                                             |
| [**GetCurrentPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)<br/>                                     | Obtiene la información del paquete para el proceso que realiza la llamada.<br/>                                                                                                 |
| [**GetCurrentPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo2)<br/>                                     | Obtiene la información del paquete para el proceso que realiza la llamada, con la opción de especificar el tipo de carpeta del paquete.<br/>                                                                                               |
| [**GetCurrentPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath)<br/>                                     | Obtiene la ruta de acceso del paquete para el proceso que realiza la llamada.<br/>                                                                                                        |
| [**GetCurrentPackagePath2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath2)<br/>                                     | Obtiene la ruta de acceso del paquete para el proceso que realiza la llamada, con la opción de especificar el tipo de carpeta del paquete.<br/>                                                                                                        |
| [**GetPackageApplicationIds**](/windows/desktop/api/AppModel/nf-appmodel-getpackageapplicationids)<br/>                               | Obtiene los identificadores de las aplicaciones en el paquete especificado.<br/>                                                                                                        |
| [**GetPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilyname)<br/>                                       | Obtiene el nombre de familia del paquete para el proceso especificado.<br/>                                                                                               |
| [**GetPackageFamilyNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilynamefromtoken)<br/>                     | Obtiene el nombre de familia del paquete para el token especificado.<br/>                                                                                                 |
| [**GetPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullname)<br/>                                           | Obtiene el nombre completo del paquete para el proceso especificado.<br/>                                                                                                 |
| [**GetPackageFullNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullnamefromtoken)<br/>                         | Obtiene el nombre completo del paquete para el token especificado.<br/>                                                                                                   |
| [**GetPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getpackageid)<br/>                                                       | Obtiene el identificador de paquete (ID.) del proceso especificado.<br/>                                                                                           |
| [**GetPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)<br/>                                                   | Obtiene la información de paquete para el paquete especificado.<br/>                                                                                               |
| [**GetPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo2)<br/>                                                   | Obtiene la información de paquete para el paquete especificado, con la opción de especificar el tipo de carpeta del paquete.<br/>                                                                                               |
| [**Llamó a getpackagepath**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepath)<br/>                                                   | Obtiene la ruta de acceso del paquete especificado.<br/>                                                                                                              |
| [**GetPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname)<br/>                               | Obtiene la ruta de acceso del paquete especificado.<br/>                                                                                                               |
| [**GetPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname2)<br/>                               | Obtiene la ruta de acceso del paquete especificado, con la opción de especificar el tipo de carpeta del paquete.<br/>                                                                                                               |
| [**GetPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-getpackagesbypackagefamily)<br/>                           | Obtiene los paquetes con el nombre de familia especificado para el usuario actual. <br/>                                                                               |
| [**GetStagedPackageOrigin**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackageorigin)<br/>                                   | Obtiene el origen del paquete especificado.<br/>                                                                                                             |
| [**GetStagedPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname)<br/>                   | Obtiene la ruta de acceso del paquete provisional especificado.<br/>                                                                                                        |
| [**GetStagedPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname2)<br/>                   | Obtiene la ruta de acceso del paquete provisional especificado, con la opción de especificar el tipo de carpeta del paquete.<br/>                                                                                                        |
| [**OpenPackageInfoByFullName**](/windows/desktop/api/AppModel/nf-appmodel-openpackageinfobyfullname)<br/>                             | Abre la información de paquete del paquete especificado.<br/>                                                                                               |
| [**PackageFamilyNameFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromfullname)<br/>                     | Obtiene el nombre de familia del paquete para el nombre completo del paquete especificado.<br/>                                                                                     |
| [**PackageFamilyNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromid)<br/>                                 | Obtiene el nombre de familia del paquete para el identificador de paquete especificado.<br/>                                                                                    |
| [**PackageFullNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefullnamefromid)<br/>                                     | Obtiene el nombre completo del paquete para el identificador de paquete especificado (ID.).<br/>                                                                                 |
| [**PackageIdFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)<br/>                                     | Obtiene el identificador de paquete (ID.) del nombre completo del paquete especificado.<br/>                                                                                 |
| [**PackageNameAndPublisherIdFromFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-packagenameandpublisheridfromfamilyname)<br/> | Obtiene el nombre del paquete y el identificador del publicador (ID.) para el nombre de familia de paquete especificado.<br/>                                                            |
| [**ParseApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-parseapplicationusermodelid)<br/>                         | Deconstruye un [identificador de modelo de usuario](appx-packaging-glossary.md) de la aplicación en el nombre de familia del paquete y el identificador de la aplicación relativa del paquete (PRAID).<br/>      |
| [**PackageOrigin**](/windows/desktop/api/AppModel/ne-appmodel-packageorigin)<br/>                                                     | Especifica el origen de un paquete. <br/>                                                                                                                   |
| [**Constantes de identidad**](identity-constants.md)<br/>                                           | Especifica la longitud de las cadenas para los campos de identidad del paquete.<br/>                                                                                |
| [**Constantes de paquete**](package-constants.md)<br/>                                             | Especifica cómo se van a procesar los paquetes.<br/>                                                                                                           |
| [**identificador de paquete \_**](/windows/desktop/api/AppModel/ns-appmodel-package_id)<br/>                                                          | Representa la información de identificación del paquete, como el nombre, la versión y el publicador.<br/>                                                                  |
| [**información del paquete \_**](/windows/desktop/api/AppModel/ns-appmodel-package_info)<br/>                                                      | Representa la información de identificación del paquete que incluye el identificador del paquete, el nombre completo y la ubicación de instalación.<br/>                                  |
| [**versión del paquete \_**](/windows/desktop/api/AppModel/ns-appmodel-package_version)<br/>                                                | Representa la información de versión del paquete.<br/>                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptos**
</dt> <dt>

[Implementación y paquetes de aplicaciones](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

[Glosario](appx-packaging-glossary.md)
</dt> <dt>

**Referencia**
</dt> <dt>

[Esquema del manifiesto del paquete de la aplicación](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[API de empaquetado](interfaces.md)
</dt> <dt>

[API de implementación del paquete](package-deployment-api.md)
</dt> </dl>

 

