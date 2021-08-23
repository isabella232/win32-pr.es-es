---
description: PERFIL INALÁMBRICO \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a29b02240e6daeb98713a9a58a1332b44464cafafddab1559e07915a4acaf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445095"
---
# <a name="wpd_content_type_wireless_profile"></a>PERFIL INALÁMBRICO \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD

Un objeto que describe su tipo como WPD CONTENT TYPE WIRELESS PROFILE representa \_ la información utilizada para acceder a una red \_ \_ \_ inalámbrica.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad             | Obligatorio u opcional                      |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                | Obligatorio.                                                             |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Obligatorio.                                                             |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto representa un archivo.                             |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                          | Obligatorio.                                                             |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Obligatorio.                                                             |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Obligatorio.                                                             |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                     |
| [WPD \_ OBJECT \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema). |
| [TAMAÑO DEL OBJETO \_ WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                     |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                             |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo. |
| [REFERENCIAS DE OBJETOS \_ WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.               |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                             |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                |
| [FECHA DE CREACIÓN \_ DEL \_ OBJETO WPD \_](object-properties.md)                                           | Opcional.                                                             |
| [FECHA DE MODIFICACIÓN \_ DEL OBJETO \_ WPD \_](object-properties.md)                                         | Se recomienda su uso.                                                          |
| [FECHA DE \_ CREACIÓN DEL \_ OBJETO \_ WPD](object-properties.md)                                         | Opcional.                                                             |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.            |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                             |
| [WPD \_ OBJECT \_ GENERATE \_ THUMBNAIL \_ FROM \_ RESOURCE](object-properties.md) | Opcional.                                                             |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                               | Obligatorio si no se puede eliminar el objeto.                             |
| [CONFIGURACIÓN REGIONAL \_ DEL LENGUAJE DE OBJETOS \_ \_ WPD](object-properties.md)                                                                | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                          | Obligatorio u opcional                                  | Descripción               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md) | Obligatorio si el objeto se representa mediante datos binarios. | Contiene los datos binarios. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



