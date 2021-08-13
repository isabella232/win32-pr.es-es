---
description: Escribir un objeto de encabezado ASF para un nuevo archivo
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Escribir un objeto de encabezado ASF para un nuevo archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee50adc4e3f411bca9679672b88680ab3064bc91d828e2897ae1f94e40f9f9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355215"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a>Escribir un objeto de encabezado ASF para un nuevo archivo

El objeto ContentInfo de ASF almacena la información del objeto de encabezado de ASF para un archivo. Cuando se crea o modifica un archivo ASF, se debe generar el objeto de encabezado. Para ello, la aplicación debe proporcionar el perfil de codificación del contenido al objeto ContentInfo para que conozca las características del archivo multimedia que se va a crear.

Para escribir un nuevo archivo, puede usar el objeto ContentInfo para:

-   Recopile información de encabezado del objeto de perfil del archivo que se va a crear.
-   Rellenar varios objetos de encabezado en la biblioteca de ASF mantenida internamente por Media Foundation,
-   Inicialice el [multiplexor de ASF para](asf-multiplexer.md) la generación de paquetes de datos de ASF y
-   Construya el objeto de encabezado de nivel superior en formato binario que se pueda escribir en un archivo.

Para obtener información sobre los perfiles, vea [Perfil de ASF.](asf-profile.md)

Esta sección contiene los siguientes temas:



| Tema                                                                                                              | Descripción                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Inicializar el objeto ContentInfo de un nuevo archivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md) | Describe el método [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) que inicializa el objeto ContentInfo con información de encabezado almacenada en un objeto de perfil. |
| [Establecer propiedades en el objeto ContentInfo](setting-properties-in-the-contentinfo-object.md)                   | Información sobre las distintas propiedades de configuración que se deben establecer en el objeto ContentInfo.                                                                                         |
| [Generar un nuevo objeto de encabezado ASF](generating-a-new-asf-header-object.md)                                       | Cómo generar un búfer multimedia, que contiene el objeto de encabezado ASF real del nuevo archivo, a partir del objeto ContentInfo.                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto ContentInfo de ASF](asf-contentinfo-object.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

Estructura de archivos asf
</dt> </dl>

 

 



