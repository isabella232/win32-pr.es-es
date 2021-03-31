---
title: Obtener y establecer metadatos y atributos
description: Obtener y establecer metadatos y atributos
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Media Administrador de dispositivos, atributos
- Administrador de dispositivos, atributos
- aplicaciones de escritorio, atributos
- proveedores de servicios, atributos
- Guía de programación, atributos
- attributes
- Administrador de dispositivos de Windows Media, metadatos
- Administrador de dispositivos, metadatos
- aplicaciones de escritorio, metadatos
- proveedores de servicios, metadatos
- Guía de programación, metadatos
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903577"
---
# <a name="getting-and-setting-metadata-and-attributes"></a>Obtener y establecer metadatos y atributos

Una aplicación puede obtener dos tipos de información sobre un dispositivo o almacenamiento: atributos y metadatos. Los atributos son valores booleanos más sencillos que, por lo general, describen la información del sistema de archivos, por ejemplo, si un almacenamiento tiene objetos secundarios, si se puede cambiar de nombre, leer o eliminar, etc. Los atributos se recuperan como valores de marcas mediante una llamada a [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) o [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2). Los atributos se establecen mediante una llamada a [**IWMDMStorage3:: setMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).

Una aplicación también puede solicitar datos más complejos (numéricos, de cadena u otros tipos de datos) como *metadatos*. Los valores de los metadatos se identifican mediante nombres de cadena únicos. Windows Media Administrador de dispositivos define una lista de constantes de cadena que se pueden usar para solicitar valores. Estos valores definidos se muestran en [constantes de metadatos](metadata-constants.md). Un proveedor de servicios puede definir sus propias constantes, pero una aplicación que realiza la llamada debe tener en cuenta estas definiciones para solicitar o establecer estos valores de metadatos personalizados. La aplicación solicita los metadatos mediante una llamada a [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).

Un aspecto importante de la obtención y configuración de metadatos y atributos es comprender de dónde proceden los valores recuperados. El proveedor de servicios o el dispositivo pueden obtener estos valores desde muchos lugares diferentes, entre los que se incluyen los siguientes:

-   Del encabezado del archivo. Por ejemplo, en un archivo ASF, la velocidad de bits se almacena en el encabezado del archivo.
-   De los valores establecidos explícitamente por la aplicación cuando se llama a un método. Estos valores se pueden guardar en un almacén de metadatos externo en el proveedor de servicios o en el dispositivo. Este almacén puede persistir o no cuando el dispositivo se desconecta o se apaga. Por ejemplo, las clasificaciones de recuento de juegos y de estrellas de usuario suelen almacenarse en almacenes externos en el equipo o dispositivo.
-   Examinando la información proporcionada por el sistema de archivos. Por ejemplo, si un archivo es de solo lectura o si una carpeta tiene elementos secundarios.
-   Abriendo y analizando los datos del archivo.

Es importante tener en cuentan que una propiedad puede almacenarse en más de una ubicación (dentro del encabezado de archivo y también en un almacén local) y que puede ser o no modificable. Por ejemplo, el cambio de una descripción de archivo puede ser o no persistente; Si el proveedor de servicios almacena la descripción localmente, no se conservará en el dispositivo. Del mismo modo, si la descripción del archivo se toma del encabezado del archivo, la modificación solo será persistente si el proveedor de servicios o el dispositivo se abren y modifican los datos del encabezado. La mayoría de las aplicaciones realizan un mejor intento cambiando los valores deseados, pero no dependen de las propiedades que se cambien de forma persistente.

Más información sobre cómo obtener y establecer valores en las secciones adecuadas para desarrolladores de aplicaciones y desarrolladores de proveedores de servicios más adelante en la documentación de.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas comunes a las aplicaciones y proveedores de servicios**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




