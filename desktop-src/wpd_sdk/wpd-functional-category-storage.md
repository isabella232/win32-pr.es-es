---
description: ALMACENAMIENTO DE CATEGORÍAS \_ \_ FUNCIONALES DE WPD \_
ms.assetid: 92a10de6-3e50-4042-a9b7-3c1d5944791f
title: WPD_FUNCTIONAL_CATEGORY_STORAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b16d70ebff4c61643b4d5ae0f8b333f5f9a7dc02103a32e14ded7a0ac4d8189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805954"
---
# <a name="wpd_functional_category_storage"></a>ALMACENAMIENTO DE CATEGORÍAS \_ \_ FUNCIONALES DE WPD \_

Un objeto funcional \_ WPD FUNCTIONAL \_ CATEGORY STORAGE encapsula el almacenamiento de archivos físico en el \_ dispositivo.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ DE \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                                                         |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Obligatorio.                                                                                                                                              |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio.                                                                                                                                              |
| [WPD \_ OBJECT \_ PERSISTENT \_ UNIQUE \_ ID](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                                                         |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Obligatorio.                                                                                                                                              |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Obligatorio.                                                                                                                                              |
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
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                                     | Obligatorio si no se puede eliminar el objeto.                                                                                                              |
| [CONFIGURACIÓN REGIONAL \_ DEL LENGUAJE DE OBJETOS \_ \_ WPD](object-properties.md)                                                                | Opcional.                                                                                                                                              |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE WPD \_](miscellaneous-properties.md)                      | Obligatorio. Vea [**WPD \_ CONTENT TYPE FUNCTIONAL \_ OBJECT \_ \_ (OBJETO FUNCIONAL DE**](wpd-content-type-functional-object.md) TIPO DE CONTENIDO DE WPD) para ver las categorías definidas Windows dispositivos portátiles. |
| [TIPO DE \_ ALMACENAMIENTO \_ WPD](storage-properties.md)                                                         | Obligatorio.                                                                                                                                              |
| [TIPO DE \_ SISTEMA DE ARCHIVOS DE ALMACENAMIENTO \_ \_ \_ WPD](storage-properties.md)                               | Opcional.                                                                                                                                              |
| [CAPACIDAD DE \_ ALMACENAMIENTO DE \_ WPD](storage-properties.md)                                                 | Obligatorio.                                                                                                                                              |
| [ESPACIO LIBRE \_ DE ALMACENAMIENTO \_ WPD EN \_ \_ \_ BYTES](storage-properties.md)                        | Opcional.                                                                                                                                              |
| [ESPACIO LIBRE \_ DE ALMACENAMIENTO \_ WPD EN \_ \_ \_ OBJETOS](storage-properties.md)                    | Opcional.                                                                                                                                              |
| [DESCRIPCIÓN DE \_ ALMACENAMIENTO DE \_ WPD](storage-properties.md)                                           | Opcional.                                                                                                                                              |
| [NÚMERO DE \_ SERIE DE ALMACENAMIENTO DE \_ \_ WPD](storage-properties.md)                                      | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                    | Obligatorio u opcional | Descripción                                        |
|--------------------------------------------------|----------------------|----------------------------------------------------|
| [**ICONO DE RECURSO DE WPD \_ \_**](wpd-resource-icon.md) | Opcional.            | Contiene la representación de icono para este almacenamiento. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**OBJETO FUNCIONAL \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



