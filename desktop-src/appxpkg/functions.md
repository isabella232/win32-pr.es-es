---
title: API de consulta de paquetes
description: Obtenga información sobre la API de consulta de paquetes, que puede usar para obtener información sobre los paquetes de aplicación instalados en el sistema. Cada paquete de aplicación contiene los archivos que constituyen una Windows aplicación y un archivo de manifiesto que describe el software que se va a Windows.
ms.assetid: EDDFC8B1-E224-4921-BED6-FC81711BA5BF
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 0669f6a48aff7ca2e7a9669e65405b76b29060c0b57f310021994c2c59c569e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994195"
---
# <a name="package-query-api"></a>API de consulta de paquetes

Obtenga información sobre la API de consulta de paquetes, que puede usar para obtener información sobre los paquetes de aplicación instalados en el sistema. Cada paquete de aplicación contiene los archivos que constituyen una Windows aplicación y un archivo de manifiesto que describe el software que se va a Windows.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                 | Descripción                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosePackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-closepackageinfo)<br/>                                               | Cierra una referencia a la información del paquete especificada.<br/>                                                                                              |
| [**FindPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-findpackagesbypackagefamily)<br/>                         | Busca los paquetes con el nombre de familia especificado para el usuario actual. <br/>                                                                              |
| [**FormatApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-formatapplicationusermodelid)<br/>                       | Construye un identificador [de modelo de usuario de aplicación](appx-packaging-glossary.md) a partir del nombre de familia del paquete y el identificador de aplicación relativo (PRAID) del paquete. <br/> |
| [**GetApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelid)<br/>                             | Obtiene el [identificador de modelo de usuario de](appx-packaging-glossary.md) la aplicación para el proceso especificado.<br/>                                                          |
| [**GetApplicationUserModelIdFromToken**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelidfromtoken)<br/>           | Obtiene el [identificador de modelo de usuario de](appx-packaging-glossary.md) la aplicación para el token especificado.<br/>                                                            |
| [**GetCurrentApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getcurrentapplicationusermodelid)<br/>               | Obtiene el identificador [de modelo de usuario de](appx-packaging-glossary.md) la aplicación para el proceso actual.<br/>                                                            |
| [**GetCurrentPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefamilyname)<br/>                         | Obtiene el nombre de familia del paquete para el proceso de llamada.<br/>                                                                                                 |
| [**GetCurrentPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefullname)<br/>                             | Obtiene el nombre completo del paquete para el proceso de llamada.<br/>                                                                                                   |
| [**GetCurrentPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageid)<br/>                                         | Obtiene el identificador (ID) del paquete para el proceso de llamada.<br/>                                                                                             |
| [**GetCurrentPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)<br/>                                     | Obtiene la información del paquete para el proceso de llamada.<br/>                                                                                                 |
| [**GetCurrentPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo2)<br/>                                     | Obtiene la información del paquete para el proceso de llamada, con la opción de especificar el tipo de carpeta del paquete.<br/>                                                                                               |
| [**GetCurrentPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath)<br/>                                     | Obtiene la ruta de acceso del paquete para el proceso de llamada.<br/>                                                                                                        |
| [**GetCurrentPackagePath2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath2)<br/>                                     | Obtiene la ruta de acceso del paquete para el proceso de llamada, con la opción de especificar el tipo de carpeta del paquete.<br/>                                                                                                        |
| [**GetPackageApplicationIds**](/windows/desktop/api/AppModel/nf-appmodel-getpackageapplicationids)<br/>                               | Obtiene los ID de las aplicaciones del paquete especificado.<br/>                                                                                                        |
| [**GetPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilyname)<br/>                                       | Obtiene el nombre de familia del paquete para el proceso especificado.<br/>                                                                                               |
| [**GetPackageFamilyNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilynamefromtoken)<br/>                     | Obtiene el nombre de familia del paquete para el token especificado.<br/>                                                                                                 |
| [**GetPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullname)<br/>                                           | Obtiene el nombre completo del paquete para el proceso especificado.<br/>                                                                                                 |
| [**GetPackageFullNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullnamefromtoken)<br/>                         | Obtiene el nombre completo del paquete para el token especificado.<br/>                                                                                                   |
| [**GetPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getpackageid)<br/>                                                       | Obtiene el identificador (ID) del paquete para el proceso especificado.<br/>                                                                                           |
| [**GetPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)<br/>                                                   | Obtiene la información del paquete especificado.<br/>                                                                                               |
| [**GetPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo2)<br/>                                                   | Obtiene la información del paquete especificado, con la opción de especificar el tipo de carpeta del paquete.<br/>                                                                                               |
| [**GetPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepath)<br/>                                                   | Obtiene la ruta de acceso del paquete especificado.<br/>                                                                                                              |
| [**GetPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname)<br/>                               | Obtiene la ruta de acceso del paquete especificado.<br/>                                                                                                               |
| [**GetPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname2)<br/>                               | Obtiene la ruta de acceso del paquete especificado, con la opción de especificar el tipo de carpeta del paquete.<br/>                                                                                                               |
| [**GetPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-getpackagesbypackagefamily)<br/>                           | Obtiene los paquetes con el nombre de familia especificado para el usuario actual. <br/>                                                                               |
| [**GetStagedPackageOrigin**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackageorigin)<br/>                                   | Obtiene el origen del paquete especificado.<br/>                                                                                                             |
| [**GetStagedPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname)<br/>                   | Obtiene la ruta de acceso del paquete staged especificado.<br/>                                                                                                        |
| [**GetStagedPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname2)<br/>                   | Obtiene la ruta de acceso del paquete staged especificado, con la opción de especificar el tipo de carpeta del paquete.<br/>                                                                                                        |
| [**OpenPackageInfoByFullName**](/windows/desktop/api/AppModel/nf-appmodel-openpackageinfobyfullname)<br/>                             | Abre la información del paquete especificado.<br/>                                                                                               |
| [**PackageFamilyNameFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromfullname)<br/>                     | Obtiene el nombre de familia del paquete para el nombre completo del paquete especificado.<br/>                                                                                     |
| [**PackageFamilyNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromid)<br/>                                 | Obtiene el nombre de familia del paquete para el identificador de paquete especificado.<br/>                                                                                    |
| [**PackageFullNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefullnamefromid)<br/>                                     | Obtiene el nombre completo del paquete para el identificador (ID) del paquete especificado.<br/>                                                                                 |
| [**PackageIdFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)<br/>                                     | Obtiene el identificador del paquete (ID) del nombre completo del paquete especificado.<br/>                                                                                 |
| [**PackageNameAndPublisherIdFromFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-packagenameandpublisheridfromfamilyname)<br/> | Obtiene el nombre del paquete y el identificador del publicador (ID) del nombre de familia del paquete especificado.<br/>                                                            |
| [**ParseApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-parseapplicationusermodelid)<br/>                         | Deconstruye un identificador de [modelo de usuario de aplicación](appx-packaging-glossary.md) en su nombre de familia de paquetes y el identificador de aplicación relativa del paquete (PRAID).<br/>      |
| [**PackageOrigin**](/windows/desktop/api/AppModel/ne-appmodel-packageorigin)<br/>                                                     | Especifica el origen de un paquete. <br/>                                                                                                                   |
| [**Constantes de identidad**](identity-constants.md)<br/>                                           | Especifica la longitud de las cadenas para los campos de identidad del paquete.<br/>                                                                                |
| [**Constantes de paquete**](package-constants.md)<br/>                                             | Especifica cómo se van a procesar los paquetes.<br/>                                                                                                           |
| [**ID. DE \_ PAQUETE**](/windows/desktop/api/AppModel/ns-appmodel-package_id)<br/>                                                          | Representa la información de identificación del paquete, como el nombre, la versión y el publicador.<br/>                                                                  |
| [**INFORMACIÓN DEL \_ PAQUETE**](/windows/desktop/api/AppModel/ns-appmodel-package_info)<br/>                                                      | Representa la información de identificación del paquete que incluye el identificador del paquete, el nombre completo y la ubicación de instalación.<br/>                                  |
| [**VERSIÓN DEL \_ PAQUETE**](/windows/desktop/api/AppModel/ns-appmodel-package_version)<br/>                                                | Representa la información de la versión del paquete.<br/>                                                                                                           |



 

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

 

