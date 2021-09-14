---
description: INFORMACIÓN DE REPRESENTACIÓN \_ DE \_ CATEGORÍAS FUNCIONALES \_ DE \_ WPD
ms.assetid: 84ec6f14-fe90-42a5-ba2b-6c4cc406935c
title: WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bf2a5b981b75820b566e3133faab22c2f35860
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256071"
---
# <a name="wpd_functional_category_rendering_information"></a>INFORMACIÓN DE REPRESENTACIÓN \_ DE \_ CATEGORÍAS FUNCIONALES \_ DE \_ WPD

Un objeto funcional WPD FUNCTIONAL CATEGORY RENDERING INFORMATION describe qué tipo de archivos \_ multimedia puede representar el \_ \_ \_ dispositivo.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                                                         |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Necesario.                                                                                                                                              |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Necesario.                                                                                                                                              |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                                                         |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Necesario.                                                                                                                                              |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Necesario.                                                                                                                                              |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                                                                                                      |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                                                                  |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                                                                      |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                                                                                                              |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.                                                                                  |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                                                                                                |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                                                                                              |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                                                                                              |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                                                                                 |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                                           | Opcional.                                                                                                                                              |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                                         | Se recomienda su uso.                                                                                                                                           |
| [FECHA DE CREACIÓN \_ DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                                                                                                              |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                                                                             |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                                                                                              |
| [WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE](object-properties.md) | Opcional.                                                                                                                                              |
| [EL OBJETO \_ WPD \_ SE PUEDE \_ ELIMINAR](object-properties.md)                                                                     | Obligatorio si no se puede eliminar el objeto.                                                                                                              |
| [CONFIGURACIÓN REGIONAL \_ DEL LENGUAJE DE OBJETOS \_ \_ WPD](object-properties.md)                                                                | Opcional.                                                                                                                                              |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE WPD \_](miscellaneous-properties.md)                      | Necesario. Vea WPD CONTENT TYPE FUNCTIONAL OBJECT (OBJETO [**\_ \_ \_ \_ FUNCIONAL DE**](wpd-content-type-functional-object.md) TIPO DE CONTENIDO DE WPD) para ver las categorías definidas Windows dispositivos portátiles. |
| [PERFILES DE \_ INFORMACIÓN \_ DE REPRESENTACIÓN \_ DE WPD](miscellaneous-properties.md)              | Necesario.                                                                                                                                              |
| [TIPO DE ENTRADA \_ DEL PERFIL DE INFORMACIÓN DE REPRESENTACIÓN \_ \_ \_ DE \_ WPD](miscellaneous-properties.md)                                     | Opcional.                                                                                                                                              |
| [RECURSO \_ CREATABLE DE \_ ENTRADA DEL PERFIL DE INFORMACIÓN DE REPRESENTACIÓN \_ \_ \_ DE \_ WPD](miscellaneous-properties.md)                      | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**OBJETO FUNCIONAL \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



