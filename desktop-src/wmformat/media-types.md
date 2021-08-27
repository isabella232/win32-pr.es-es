---
title: Tipos de medios para Windows SDK de formato multimedia
description: Obtenga información sobre los tipos de medios que puede usar el SDK Windows Media Format. Los tipos de medios son valores GUID asignados a constantes en el SDK.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows SDK de formato multimedia, tipos de medios
- Formato de sistemas avanzados (ASF), tipos de medios
- ASF (formato de sistemas avanzados),tipos de medios
- tipos de medios, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84974391a7e044367fd298598181d43447cfac4bec1829b9e5ddb0b90ae27ea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027493"
---
# <a name="media-types-for-windows-media-format-sdk"></a>Tipos de medios para Windows SDK de formato multimedia

Los tipos de medios identifican los distintos tipos de medios que puede usar el SDK Windows Media Format. Todos los tipos de medios son valores GUID que se han asignado a constantes en el SDK. Los valores GUID representados por las constantes enumeradas en esta sección se enumeran en la [sección Identificadores](media-type-identifiers.md) de tipo multimedia de esta referencia.

En la tabla siguiente se enumeran los tipos de medios principales. Estas constantes definen la clasificación de alto nivel de los medios digitales admitidos por el SDK Windows Media Format.



| Tipo principal                | Descripción                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| Vídeo \_ WMMEDIATYPE        | Una secuencia de vídeo.                                                                                         |
| WMMEDIATYPE \_ Audio        | Una secuencia de audio.                                                                                        |
| WMMEDIATYPE \_ Script       | Secuencia de scripts.                                                                                        |
| WMMEDIATYPE \_ FileTransfer | Secuencia que contiene archivos de datos. Las secuencias web, que constan de archivos HTML, también tienen este tipo principal. |
| Imagen \_ WMMEDIATYPE        | Secuencia de imagen JPEG para un archivo de audio ilustrado (como en una presentación de diapositivas).                                 |
| Texto \_ WMMEDIATYPE         | Secuencia de texto.                                                                                          |



 

Además de los tipos de medios principales admitidos explícitamente, puede crear sus propios tipos de datos arbitrarios. Para los tipos de datos arbitrarios personalizados, debe asegurarse de que el GUID que use no coincida con un tipo principal existente.

Una secuencia multimedia a menudo tendrá un subtipo además de su tipo principal. En las secciones siguientes se enumeran los subtipos admitidos.



| Sección                                                        | Descripción                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Subtipos de medios sin comprimir](uncompressed-media-subtypes.md) | Describe los subtipos disponibles para medios sin comprimir. Estos son los tipos asociados normalmente a los medios de entrada o salida.              |
| [Subtipos de medios comprimidos](compressed-media-subtypes.md)     | Describe los subtipos disponibles para medios comprimidos. Estos son los tipos asociados normalmente a medios en una secuencia dentro de un archivo ASF. |
| [Formatos de entrada de vídeo](video-input-formats.md)                 | Enumera los formatos de vídeo aceptados como entradas para el códec Windows Media Video 9.                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de tipo de medio**](media-type-identifiers.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 




