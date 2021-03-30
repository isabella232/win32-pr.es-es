---
description: Las siguientes propiedades de información de resumen se deben definir en cada paquete de instalación, mediante una herramienta de software para tener acceso a la interfaz IStream de la secuencia de información de resumen.
ms.assetid: 9775959f-5ab2-43cd-8cc8-9d81945b4ec6
title: Agregar información de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26486e0082a05b05fbdc9609881083e10cddb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156348"
---
# <a name="adding-summary-information"></a>Agregar información de Resumen

Las siguientes propiedades de información de resumen se deben definir en cada paquete de instalación, mediante una herramienta de software para tener acceso a la interfaz **IStream** de la [secuencia de información de Resumen](summary-information-stream.md). Por ejemplo, puede usar la herramienta Msiinfo.exe proporcionada con el SDK de Windows Installer para establecer estas propiedades. Si no se establecen estas propiedades, el paquete no pasará la [validación del paquete](package-validation.md).



| Propiedad información de Resumen                                                   | Datos                                   | Notas                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Plantilla**](template-summary.md)(plataforma e idioma)<br/>         | ; 1033                                  | Plataforma y lenguaje usados por la base de datos. Si falta la especificación de la plataforma en el valor de propiedad de Resumen de la [**plantilla**](template-summary.md) , el instalador asume la arquitectura de Intel. La propiedad [**ProductLanguage**](productlanguage.md) de la base de datos se usa normalmente para esta propiedad de resumen. El identificador de idioma del ejemplo indica que el paquete utiliza el Inglés de EE. UU. |
| [**Número de revisión**](revision-number-summary.md)(código de paquete)<br/>    | {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} | Es el [GUID](guid.md) del código de paquete que identifica de forma única el paquete de ejemplo. Si reproduce este ejemplo, use una utilidad como GUIDGEN para generar un GUID diferente para el paquete. Los resultados de GUIDGEN contienen caracteres en minúsculas, tenga en cuenta que debe cambiar todos los caracteres en minúsculas a mayúsculas por un código de paquete válido. Vea [códigos de paquete](package-codes.md).             |
| [**Recuento de páginas**](page-count-summary.md)(versión de instalador mínima)<br/> | 200                                    | Para un mínimo Windows Installer 2,0, esta propiedad se debe establecer en el entero 200.                                                                                                                                                                                                                                                                                                                 |
| [**Recuento de palabras**](word-count-summary.md)(tipo de origen)<br/>            | 0                                      | El tipo de origen global del paquete es Long file names y Uncompressed. Vea [orígenes comprimidos y sin comprimir](compressed-and-uncompressed-sources.md) y la descripción de la columna atributos de la [tabla de archivos](file-table.md) para obtener más información.                                                                                                                                |



 

Las propiedades de flujo de información de Resumen restantes no son necesarias, pero se deben establecer para el ejemplo MNP2000.msi.



| Propiedad información de Resumen                                 | Datos                                                                             | Notas                                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Title**](title-summary.md)                               | Base de datos de instalación                                                            | Informa a los usuarios de que esta base de datos es para una instalación en lugar de una transformación o una revisión.                        |
| [**Asunto**](subject-summary.md)                           | MNP2000                                                                          | Los exploradores de archivos pueden mostrar esto como el producto que se va a instalar con esta base de datos.                                  |
| [**Palabras clave**](keywords-summary.md)                         | Instalador, MSI, base de datos                                                         | Los exploradores de archivos que admiten la búsqueda de palabras clave pueden buscar estas palabras.                                    |
| [**Autor**](author-summary.md)                             | Microsoft Corporation                                                            | Nombre del fabricante del producto.                                                                                |
| [**Comentarios**](comments-summary.md)                         | Esta base de datos del instalador contiene la lógica y los datos necesarios para instalar el Bloc de notas. | Informa a los usuarios acerca del propósito de esta base de datos.                                                                  |
| [**Creando aplicación**](creating-application-summary.md) | Orcas                                                                             | Aplicación utilizada para crear la base de datos de instalación. En el ejemplo se especifica el editor de bases de datos Orca como ejemplo. |
| [**Seguridad**](security-summary.md)                         | 0                                                                                | La base de datos de ejemplo no tiene restricciones de lectura y escritura.                                                                    |



 

No es necesario el conjunto de propiedades fecha de la última vez [**que se guardaron**](last-saved-by-summary.md), fecha y hora de la [**última actualización**](last-saved-time-date-summary.md), [**crear hora/fecha**](create-time-date-summary.md), [**última impresión**](last-printed-summary.md), [**recuento de caracteres**](character-count-summary.md)y Resumen de [**Página de códigos**](codepage-summary.md) para completar esta base de datos de ejemplo. El ejemplo se basa en la herramienta de edición de bases de datos para establecer y actualizar estas propiedades opcionales.

Por ejemplo, para usar MsiInfo para agregar la información de resumen al ejemplo, cambie al directorio que contiene la base de datos y use la siguiente línea de comandos. No vuelva a usar el identificador de paquete de ejemplo que se muestra a continuación.

**Msiinfo.exe MNP2000.msi-T "base de datos de instalación"-J Subject-A "Microsoft Corporation"-K "Installer, MSI, Database"-O "esta base de datos del instalador contiene la lógica y los datos necesarios para instalar el Bloc de notas."-P; 1033-V {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3}-G 200-W 0-N Orca-U 0**

Para obtener más información sobre la información de Resumen, vea [acerca de la secuencia de información de Resumen](about-the-summary-information-stream.md), [uso de la secuencia de información de Resumen](using-the-summary-information-stream.md)y referencia de flujo de información de [Resumen](summary-information-stream-reference.md).

Vea el [conjunto](summary-information-stream-property-set.md) de propiedades de la secuencia de información de resumen para obtener una lista completa de todas las propiedades de información de Resumen y [descripciones de propiedades de Resumen](summary-property-descriptions.md) para su descripción.

[Continuar](importing-the-user-interface.md)

 

 




