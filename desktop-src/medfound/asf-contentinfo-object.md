---
description: Objeto ContentInfo de ASF
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Objeto ContentInfo de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b42baffa65b63857509e6fcc94a5649d8968f3bd372475ef38ced6a004c1a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881264"
---
# <a name="asf-contentinfo-object"></a>Objeto ContentInfo de ASF

El objeto *ContentInfo de* ASF almacena información del objeto de encabezado ASF de un archivo. Una aplicación puede usar el objeto ContentInfo para los siguientes fines:

-   Lea el objeto de encabezado de un archivo multimedia existente. En este caso, el objeto ContentInfo analiza el objeto de encabezado y almacena información sobre el archivo de características. Media Foundation expone varias de estas propiedades a través de atributos e interfaces. Se describen en atributos [Media Foundation para objetos de encabezado de ASF.](media-foundation-attributes-for-asf-header-objects.md)
-   Escriba información de encabezado y construya un objeto de encabezado para un nuevo archivo.
-   Inicialice otros objetos de ASF, como el divisor [ASF,](asf-splitter.md)el [multiplexor](asf-multiplexer.md)de ASF y el indexador de ASF, mientras lee o escribe un archivo multimedia.

Para obtener información sobre la estructura de un archivo ASF, vea [ASF File Structure](asf-file-structure.md).

## <a name="creating-the-contentinfo-object"></a>Crear el objeto ContentInfo

Para crear una nueva instancia del objeto ContentInfo, llame a la [**función MFCreateASFContentInfo.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) Este método devuelve un puntero a un objeto ContentInfo vacío que se debe inicializar para trabajar con un archivo ASF específico. Dependiendo de si la aplicación está leyendo un archivo existente o escribiendo un nuevo archivo ASF, debe llamar a [**IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) o [**a IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para rellenar el objeto vacío.

Para obtener más información sobre estas llamadas a métodos, vea los temas siguientes:

-   [Leer el objeto de encabezado ASF de un archivo existente](reading-the-asf-header-object-of-an-existing-file.md)
-   [Obtener información de objetos de encabezado de ASF](getting-information-from-asf-header-objects.md)
-   [Escribir un objeto de encabezado ASF para un nuevo archivo](writing-an-asf-header-object-for-a-new-file.md)
-   [Media Foundation atributos para objetos de encabezado asf](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de ASF de WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



