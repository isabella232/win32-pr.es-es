---
description: Las siguientes propiedades de información de resumen deben definirse en cada paquete de instalación, mediante una herramienta de software para acceder a la interfaz Istream del flujo de información de resumen.
ms.assetid: 9775959f-5ab2-43cd-8cc8-9d81945b4ec6
title: Agregar información de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26486e0082a05b05fbdc9609881083e10cddb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159193"
---
# <a name="adding-summary-information"></a>Agregar información de resumen

Las siguientes propiedades de información de resumen deben definirse en cada paquete de instalación, mediante una herramienta de software para acceder a la **interfaz Istream** del [flujo de información de resumen](summary-information-stream.md). Por ejemplo, puede usar la herramienta que Msiinfo.exe con el SDK Windows Installer para establecer estas propiedades. Si no se establecen estas propiedades, el paquete no pasará la [validación del paquete](package-validation.md).



| Propiedad Información de resumen                                                   | Datos                                   | Notas                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Plantilla**](template-summary.md)(plataforma e idioma)<br/>         | ;1033                                  | Plataforma y lenguaje usados por la base de datos. Si falta la especificación de la plataforma en el [**valor de la propiedad Resumen**](template-summary.md) de plantilla, el instalador asume la arquitectura intel. La [**propiedad ProductLanguage de**](productlanguage.md) la base de datos se usa normalmente para esta propiedad de resumen. El identificador de idioma del ejemplo indica que el paquete usa el inglés de EE. UU. |
| [**Número de revisión**](revision-number-summary.md)(código del paquete)<br/>    | {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} | Este es el GUID del código [del paquete](guid.md) que identifica de forma única el paquete de ejemplo. Si reproduce este ejemplo, use una utilidad como GUIDGEN para generar un GUID diferente para el paquete. Los resultados de GUIDGEN contienen caracteres en minúscula, tenga en cuenta que debe cambiar todos los caracteres en minúsculas a mayúsculas para un código de paquete válido. Vea [Códigos de paquete](package-codes.md).             |
| [**Recuento de páginas**](page-count-summary.md)(versión mínima del instalador)<br/> | 200                                    | Para un valor Windows Installer 2.0, esta propiedad debe establecerse en el entero 200.                                                                                                                                                                                                                                                                                                                 |
| [**Recuento de palabras**](word-count-summary.md)(tipo de origen)<br/>            | 0                                      | El tipo de origen global del paquete son nombres de archivo largos y sin comprimir. Vea [Orígenes comprimidos y sin comprimir](compressed-and-uncompressed-sources.md) y la descripción de la columna Atributos de la tabla [Archivo](file-table.md) para obtener más información.                                                                                                                                |



 

Las propiedades restantes del flujo de información de resumen no son necesarias, pero deben establecerse para el MNP2000.msi ejemplo.



| Propiedad Información de resumen                                 | Datos                                                                             | Notas                                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Título**](title-summary.md)                               | Base de datos de instalación                                                            | Informa a los usuarios de que esta base de datos es para una instalación en lugar de una transformación o una revisión.                        |
| [**Subject**](subject-summary.md)                           | MNP2000                                                                          | Los exploradores de archivos pueden mostrar esto como el producto que se va a instalar con esta base de datos.                                  |
| [**Palabras clave**](keywords-summary.md)                         | Instalador, MSI, base de datos                                                         | Los exploradores de archivos que son capaces de buscar palabras clave pueden buscar estas palabras.                                    |
| [**Autor**](author-summary.md)                             | Microsoft Corporation                                                            | Nombre del fabricante del producto.                                                                                |
| [**Comentarios**](comments-summary.md)                         | Esta base de datos del instalador contiene la lógica y los datos necesarios para instalar Bloc de notas. | Informa a los usuarios sobre el propósito de esta base de datos.                                                                  |
| [**Creación de una aplicación**](creating-application-summary.md) | Orca                                                                             | Aplicación utilizada para crear la base de datos de instalación. El ejemplo especifica el editor de bases de datos orca como ejemplo. |
| [**Seguridad**](security-summary.md)                         | 0                                                                                | La base de datos de ejemplo es de lectura y escritura sin restricciones.                                                                    |



 

No necesita establecer las propiedades de resumen Last [**Saved By**](last-saved-by-summary.md), Last [**Saved Time/Date**](last-saved-time-date-summary.md), [**Create Time/Date**](create-time-date-summary.md), [**Last Printed**](last-printed-summary.md), [**Character Count**](character-count-summary.md)y [**Codepage**](codepage-summary.md) para completar esta base de datos de ejemplo. El ejemplo se basa en la herramienta de edición de base de datos para establecer y actualizar estas propiedades opcionales.

Por ejemplo, para usar MsiInfo para agregar la información de resumen al ejemplo, cambie al directorio que contiene la base de datos y use la siguiente línea de comandos. No reutilice el identificador de paquete de ejemplo que se muestra a continuación.

**Msiinfo.exe MNP2000.msi -T "Base de datos de instalación" -J Asunto -A "Microsoft Corporation" -K "Instalador, MSI, Base de datos" -O "Esta base de datos del instalador contiene la lógica y los datos necesarios para instalar Bloc de notas." -P ;1033 -V {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} -G 200 -W 0 -N Orca -U 0**

Para obtener más información sobre la información de resumen, vea [Acerca](about-the-summary-information-stream.md)de la secuencia de información de resumen , [Uso](using-the-summary-information-stream.md)de la secuencia de información de resumen y [Referencia de flujo de información de resumen](summary-information-stream-reference.md).

Consulte Conjunto [de propiedades de](summary-information-stream-property-set.md) secuencia de información de resumen para obtener una lista completa de todas las propiedades de información de resumen y Descripciones de propiedades de [resumen](summary-property-descriptions.md) para obtener su descripción.

[Continuar](importing-the-user-interface.md)

 

 




