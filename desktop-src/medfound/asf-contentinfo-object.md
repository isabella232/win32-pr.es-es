---
description: Objeto ContentInfo de ASF
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Objeto ContentInfo de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696187"
---
# <a name="asf-contentinfo-object"></a>Objeto ContentInfo de ASF

El objeto *ContentInfo* de ASF almacena información del objeto de encabezado ASF de un archivo. Una aplicación puede utilizar el objeto ContentInfo para los siguientes fines:

-   Lea el objeto de encabezado de un archivo multimedia existente. En este caso, el objeto ContentInfo analiza el objeto de encabezado y almacena información sobre el archivo de características. Media Foundation expone algunas de estas propiedades a través de atributos e interfaces. Se describen en [Media Foundation atributos para los objetos de encabezado ASF](media-foundation-attributes-for-asf-header-objects.md).
-   Escribir información de encabezado y construir un objeto de encabezado para un archivo nuevo.
-   Inicialice otros objetos ASF, como el [separador](asf-splitter.md)ASF, el [multiplexor ASF](asf-multiplexer.md)y el indexador ASF, al leer o escribir un archivo multimedia.

Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).

## <a name="creating-the-contentinfo-object"></a>Crear el objeto ContentInfo

Para crear una nueva instancia del objeto ContentInfo, llame a la función [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) . Este método devuelve un puntero a un objeto ContentInfo vacío que se debe inicializar para que funcione con un archivo ASF específico. En función de si la aplicación Lee un archivo existente o escribe un nuevo archivo ASF, debe llamar a [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) o [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para rellenar el objeto vacío.

Para obtener más información acerca de estas llamadas a métodos, vea los temas siguientes:

-   [Leer el objeto de encabezado ASF de un archivo existente](reading-the-asf-header-object-of-an-existing-file.md)
-   [Obtener información de los objetos de encabezado ASF](getting-information-from-asf-header-objects.md)
-   [Escribir un objeto de encabezado ASF para un nuevo archivo](writing-an-asf-header-object-for-a-new-file.md)
-   [Media Foundation atributos para los objetos de encabezado ASF](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de WMContainer ASF](wmcontainer-asf-components.md)
</dt> </dl>

 

 



