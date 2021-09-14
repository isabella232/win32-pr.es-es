---
title: Obtención y configuración de metadatos y atributos
description: Obtención y configuración de metadatos y atributos
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Elementos Administrador de dispositivos,atributos
- Administrador de dispositivos,attributes
- aplicaciones de escritorio, atributos
- proveedores de servicios, atributos
- guía de programación, atributos
- attributes
- Windows Media Administrador de dispositivos,metadata
- Administrador de dispositivos,metadata
- aplicaciones de escritorio, metadatos
- proveedores de servicios, metadatos
- guía de programación, metadatos
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890300"
---
# <a name="getting-and-setting-metadata-and-attributes"></a>Obtención y configuración de metadatos y atributos

Una aplicación puede obtener dos tipos de información sobre un almacenamiento o dispositivo: atributos y metadatos. Los atributos son valores booleanos más sencillos que generalmente describen la información del sistema de archivos, como si un almacenamiento tiene objetos secundarios, si se puede cambiar el nombre, leer o eliminar, y así sucesivamente. Los atributos se recuperan como valores de marcas mediante una llamada [**a IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) o [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2). Los atributos se establecen mediante una [**llamada a IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).

Una aplicación también puede solicitar datos más complejos (numéricos, de cadena u otros tipos de datos) como *metadatos.* Los valores de metadatos se identifican mediante nombres de cadena únicos. Windows Los Administrador de dispositivos definen una lista de constantes de cadena que se pueden usar para solicitar valores; Estos valores definidos se enumeran en [Constantes de metadatos](metadata-constants.md). Un proveedor de servicios puede definir sus propias constantes, pero una aplicación que realiza la llamada debe tener en cuenta estas definiciones para solicitar o establecer estos valores de metadatos personalizados. La aplicación solicita metadatos mediante una llamada [**a IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).

Un aspecto importante de la obtención y configuración de metadatos y atributos es comprender de dónde proceden los valores recuperados. El proveedor de servicios o el dispositivo pueden obtener estos valores desde muchos lugares diferentes, incluidos los siguientes:

-   Desde el encabezado de archivo. Por ejemplo, en un archivo ASF, la velocidad de bits se almacena en el encabezado del archivo.
-   A partir de los valores establecidos explícitamente por la aplicación al llamar a un método . Estos valores se pueden guardar en un almacén de metadatos externo en el proveedor de servicios o el dispositivo. Este almacén puede o no persistir cuando el dispositivo se desconecta o se apaga. Por ejemplo, el recuento de reproducción y las clasificaciones de estrellas de usuario se almacenan normalmente en almacenes externos en el equipo o dispositivo.
-   Mediante el examen de la información proporcionada por el sistema de archivos. Por ejemplo, si un archivo es de solo lectura o si una carpeta tiene secundarios.
-   Abriendo y analizando los datos del archivo.

Es importante tener en cuenta que una propiedad puede almacenarse en más de una ubicación (dentro del encabezado de archivo y también en un almacén local) y que puede o no ser modificable. Por ejemplo, cambiar una descripción de archivo puede ser persistente o no; si el proveedor de servicios almacena la descripción localmente, no se conservará en el dispositivo. De forma similar, si la descripción del archivo se toma del encabezado de archivo, modificarlo solo será persistente si se abre el proveedor de servicios o el dispositivo y modifica los datos del encabezado. La mayoría de las aplicaciones hacen un mejor intento cambiando los valores deseados, pero no dependen de ninguna propiedad que se cambie de forma persistente.

Más información sobre cómo obtener y establecer valores se proporciona en las secciones adecuadas para desarrolladores de aplicaciones y desarrolladores de proveedores de servicios más adelante en la documentación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas comunes para aplicaciones y proveedores de servicios**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




