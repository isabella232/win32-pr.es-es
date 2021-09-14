---
description: El código del paquete de actualización debe cambiarse del del producto original.
ms.assetid: 786e864a-93e0-4ea6-adab-e87afbdd6ac2
title: Actualizar la información de resumen de una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9bee3457b9ebbe0264d569f37d8ed5a3e372df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254139"
---
# <a name="updating-summary-information-for-an-upgrade"></a>Actualizar la información de resumen de una actualización

El código del paquete de actualización debe cambiarse del del producto original. El código del paquete se almacena en la [**propiedad Resumen del número de revisión.**](revision-number-summary.md) Para obtener más información, vea [Códigos de paquete.](package-codes.md) Use Msiinfo.exe, u otro editor, para cambiar la información de resumen de MNP2001.msi como se describe en [Agregar información de resumen](adding-summary-information.md).



| Propiedad Información de resumen                                                   | Datos                                                                             | Notas                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Plantilla**](template-summary.md)(plataforma e idioma)<br/>         | ;1033                                                                            | Plataforma y lenguaje usados por la base de datos. Si falta la especificación de la plataforma en el [**valor de la**](template-summary.md) propiedad Resumen de plantilla, el instalador asume la arquitectura de Intel. La [**propiedad ProductLanguage**](productlanguage.md) de la base de datos se usa normalmente para esta propiedad de resumen. El identificador de idioma del ejemplo indica que el paquete usa inglés de EE. UU. |
| [**Número de revisión**](revision-number-summary.md)(código de paquete)<br/>    | {A0EC5348-1D02-4FF6-93F5-61BD7AC1772E}                                           | Este es el GUID del código [del paquete](guid.md) que identifica de forma única el paquete de ejemplo. Si reproduce este ejemplo, use una utilidad como GUIDGEN para generar un GUID diferente para el paquete. Los resultados de GUIDGEN contienen caracteres en minúscula, tenga en cuenta que debe cambiar todos los caracteres en minúsculas a mayúsculas para un código de paquete válido.                                                     |
| [**Recuento de páginas**](page-count-summary.md)(versión mínima del instalador)<br/> | 200                                                                              | Para una versión Windows installer 2.0, esta propiedad debe establecerse en el entero 200.                                                                                                                                                                                                                                                                                                         |
| [**Recuento de palabras**](word-count-summary.md)(tipo de origen)<br/>            | 0                                                                                | El tipo de origen global del paquete son nombres de archivo largos y sin comprimir. Para obtener más información, vea [Orígenes comprimidos](compressed-and-uncompressed-sources.md) y sin comprimir y la descripción de la columna Atributos de la [tabla File](file-table.md).                                                                                                                               |
| [**Título**](title-summary.md)                                                 | Base de datos de instalación                                                            | Informa a los usuarios de que esta base de datos es para una instalación en lugar de una transformación o una revisión.                                                                                                                                                                                                                                                                                                          |
| [**Subject**](subject-summary.md)                                             | MNP2001                                                                          | Los exploradores de archivos pueden mostrar esto como el producto que se va a instalar con esta base de datos.                                                                                                                                                                                                                                                                                                                    |
| [**Palabras clave**](keywords-summary.md)                                           | Instalador, MSI, base de datos                                                         | Los exploradores de archivos que son capaces de buscar palabras clave pueden buscar estas palabras.                                                                                                                                                                                                                                                                                                                      |
| [**Autor**](author-summary.md)                                               | Microsoft Corporation                                                            | Nombre del fabricante del producto.                                                                                                                                                                                                                                                                                                                                                                  |
| [**Comentarios**](comments-summary.md)                                           | Esta base de datos del instalador contiene la lógica y los datos necesarios para instalar Bloc de notas. | Informa a los usuarios sobre el propósito de esta base de datos.                                                                                                                                                                                                                                                                                                                                                    |
| [**Creación de una aplicación**](creating-application-summary.md)                   | Orca                                                                             | Aplicación utilizada para crear la base de datos de instalación. En el ejemplo se especifica el editor de base de datos orca como ejemplo.                                                                                                                                                                                                                                                                                   |
| [**Seguridad**](security-summary.md)                                           | 0                                                                                | La base de datos de ejemplo es de lectura y escritura sin restricciones.                                                                                                                                                                                                                                                                                                                                                      |



 

[Continuar](validating-an-installation-upgrade.md)

 

 




