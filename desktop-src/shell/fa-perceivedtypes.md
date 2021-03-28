---
description: Un tipo percibido es una categoría de tipos de archivo que le permite identificar el tipo de archivo en Windows (y aplicaciones) como imagen, audio, documento u otro tipo.
title: Tipos percibidos (el shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104998005"
---
# <a name="perceived-types-the-windows-shell"></a>Tipos percibidos (el shell de Windows)

Un tipo percibido es una categoría de tipos de archivo que le permite identificar el tipo de archivo en Windows (y aplicaciones) como imagen, audio, documento u otro tipo. Los tipos percibidos se usan para varios propósitos, incluida la determinación del tipo de carpeta, que se usa para establecer la configuración de vista predeterminada. Por ejemplo, una carpeta llena de archivos de la imagen de tipo percibida tiene asignado un modo de vista predeterminada de miniaturas.

Este tema se organiza de la siguiente manera:

-   [Acerca de los tipos percibidos](#about-perceived-types)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="about-perceived-types"></a>Acerca de los tipos percibidos

Los tipos percibidos, definidos como valores PerceivedType, son similares a los tipos de archivo, salvo que hacen referencia a amplias categorías de tipos de formato de archivo en lugar de tipos de archivo específicos. Por ejemplo, imágenes, texto, audio y comprimidos son tipos que se perciben. A los tipos de archivo (generalmente tipos de archivo públicos) se les puede asignar un tipo percibido y siempre se les debe asignar uno cada vez que haya uno que sea adecuado. Por ejemplo, los tipos de archivo de imagen. bmp,. png,. jpg y. gif son también de tipo de imagen percibida.

Los tipos percibidos predeterminados son los siguientes:

-   Carpeta
-   Texto
-   Imagen
-   Audio
-   Vídeo
-   Compressed
-   Documento
-   Sistema
-   Application
-   Gamemedia
-   Contactos

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre cómo registrar los tipos percibidos, consulte [registro de aplicaciones](app-registration.md).
-   Para obtener una lista de los tipos percibidos predeterminados, vea la enumeración [**percibida**](/windows/win32/api/shtypes/ne-shtypes-perceived) .
-   Para recuperar el tipo percibido de un archivo en función de su extensión de nombre de archivo, consulte la función [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivos](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo de archivo o tipo](prophand-content-view.md)
</dt> <dt>

[Comprobador de tipo de archivo](file-type-verifier.md)
</dt> <dt>

[Controladores de tipo de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores de programación](fa-progids.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 



