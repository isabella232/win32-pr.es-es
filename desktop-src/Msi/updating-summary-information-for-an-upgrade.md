---
description: El código de paquete del paquete de actualización debe cambiarse del producto original.
ms.assetid: 786e864a-93e0-4ea6-adab-e87afbdd6ac2
title: Actualización de la información de Resumen de una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9bee3457b9ebbe0264d569f37d8ed5a3e372df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083347"
---
# <a name="updating-summary-information-for-an-upgrade"></a>Actualización de la información de Resumen de una actualización

El código de paquete del paquete de actualización debe cambiarse del producto original. El código del paquete se almacena en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) . Para obtener más información, consulte [códigos de paquete](package-codes.md). Use Msiinfo.exe u otro editor para cambiar la información de Resumen de MNP2001.msi como se describe en [Agregar información de Resumen](adding-summary-information.md).



| Propiedad información de Resumen                                                   | Datos                                                                             | Notas                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Plantilla**](template-summary.md)(plataforma e idioma)<br/>         | ; 1033                                                                            | Plataforma y lenguaje usados por la base de datos. Si falta la especificación de la plataforma en el valor de propiedad de Resumen de la [**plantilla**](template-summary.md) , el instalador asume la arquitectura de Intel. La propiedad [**ProductLanguage**](productlanguage.md) de la base de datos se usa normalmente para esta propiedad de resumen. El identificador de idioma del ejemplo indica que el paquete utiliza el Inglés de EE. UU. |
| [**Número de revisión**](revision-number-summary.md)(código de paquete)<br/>    | {A0EC5348-1D02-4FF6-93F5-61BD7AC1772E}                                           | Es el [GUID](guid.md) del código de paquete que identifica de forma única el paquete de ejemplo. Si reproduce este ejemplo, use una utilidad como GUIDGEN para generar un GUID diferente para el paquete. Los resultados de GUIDGEN contienen caracteres en minúsculas, tenga en cuenta que debe cambiar todos los caracteres en minúsculas a mayúsculas por un código de paquete válido.                                                     |
| [**Recuento de páginas**](page-count-summary.md)(versión de instalador mínima)<br/> | 200                                                                              | Para una versión mínima Windows Installer 2,0, esta propiedad se debe establecer en el entero 200.                                                                                                                                                                                                                                                                                                         |
| [**Recuento de palabras**](word-count-summary.md)(tipo de origen)<br/>            | 0                                                                                | El tipo de origen global del paquete es Long file names y Uncompressed. Para obtener más información, vea [orígenes comprimidos y sin comprimir](compressed-and-uncompressed-sources.md) y la descripción de la columna atributos de la [tabla archivo](file-table.md).                                                                                                                               |
| [**Title**](title-summary.md)                                                 | Base de datos de instalación                                                            | Informa a los usuarios de que esta base de datos es para una instalación en lugar de una transformación o una revisión.                                                                                                                                                                                                                                                                                                          |
| [**Asunto**](subject-summary.md)                                             | MNP2001                                                                          | Los exploradores de archivos pueden mostrar esto como el producto que se va a instalar con esta base de datos.                                                                                                                                                                                                                                                                                                                    |
| [**Palabras clave**](keywords-summary.md)                                           | Instalador, MSI, base de datos                                                         | Los exploradores de archivos que admiten la búsqueda de palabras clave pueden buscar estas palabras.                                                                                                                                                                                                                                                                                                                      |
| [**Autor**](author-summary.md)                                               | Microsoft Corporation                                                            | Nombre del fabricante del producto.                                                                                                                                                                                                                                                                                                                                                                  |
| [**Comentarios**](comments-summary.md)                                           | Esta base de datos del instalador contiene la lógica y los datos necesarios para instalar el Bloc de notas. | Informa a los usuarios acerca del propósito de esta base de datos.                                                                                                                                                                                                                                                                                                                                                    |
| [**Creando aplicación**](creating-application-summary.md)                   | Orcas                                                                             | Aplicación utilizada para crear la base de datos de instalación. En el ejemplo se especifica el editor de bases de datos Orca como ejemplo.                                                                                                                                                                                                                                                                                   |
| [**Seguridad**](security-summary.md)                                           | 0                                                                                | La base de datos de ejemplo no tiene restricciones de lectura y escritura.                                                                                                                                                                                                                                                                                                                                                      |



 

[Continuar](validating-an-installation-upgrade.md)

 

 




