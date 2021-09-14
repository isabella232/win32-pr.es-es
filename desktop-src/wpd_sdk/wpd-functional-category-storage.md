---
description: ALMACENAMIENTO DE CATEGORÍAS \_ \_ FUNCIONALES DE \_ WPD
ms.assetid: 92a10de6-3e50-4042-a9b7-3c1d5944791f
title: WPD_FUNCTIONAL_CATEGORY_STORAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3000c63207286bc1dae153e3f930231909e92f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266783"
---
# <a name="wpd_functional_category_storage"></a>ALMACENAMIENTO DE CATEGORÍAS \_ \_ FUNCIONALES DE \_ WPD

Un objeto funcional \_ WPD FUNCTIONAL \_ CATEGORY STORAGE encapsula el almacenamiento de archivos físico en el \_ dispositivo.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDENTIFICADOR DE OBJETO \_ \_ WPD](object-properties.md)                                                                | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                                                         |
| [IDENTIFICADOR PRIMARIO DEL \_ OBJETO \_ \_ WPD](object-properties.md)                                                 | Necesario.                                                                                                                                              |
| [NOMBRE DE OBJETO \_ \_ WPD](object-properties.md)                                                            | Necesario.                                                                                                                                              |
| [IDENTIFICADOR ÚNICO \_ PERSISTENTE \_ DEL OBJETO \_ \_ WPD](object-properties.md)                          | Obligatorio, de solo lectura. Un cliente no puede establecer esta propiedad, incluso en el momento de la creación.                                                                         |
| [FORMATO DE OBJETO \_ \_ WPD](object-properties.md)                                                        | Necesario.                                                                                                                                              |
| [TIPO DE CONTENIDO \_ DE \_ OBJETO \_ WPD](object-properties.md)                                           | Necesario.                                                                                                                                              |
| [\_ISHIDDEN DEL \_ OBJETO WPD](object-properties.md)                                                    | Obligatorio si el objeto está oculto.                                                                                                                      |
| [ISSYSTEM DEL \_ OBJETO \_ WPD](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                                                                  |
| [TAMAÑO DEL OBJETO \_ \_ WPD](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                                                                      |
| [NOMBRE DE ARCHIVO \_ \_ ORIGINAL DEL OBJETO \_ \_ WPD](object-properties.md)                              | Obligatorio si el objeto representa un archivo.                                                                                                              |
| [OBJETO WPD \_ \_ NO \_ CONSUMIBLE](object-properties.md)                                       | Se recomienda si el objeto no está pensado para el consumo por parte del dispositivo.                                                                                  |
| [REFERENCIAS A OBJETOS \_ \_ WPD](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.                                                                                                |
| [PALABRAS CLAVE DE \_ OBJETO \_ WPD](object-properties.md)                                                    | Opcional.                                                                                                                                              |
| [IDENTIFICADOR DE SINCRONIZACIÓN \_ DE \_ OBJETOS \_ WPD](object-properties.md)                                                     | Opcional.                                                                                                                                              |
| [EL OBJETO \_ WPD \_ ESTÁ PROTEGIDO CON \_ \_ DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                                                                                 |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                           | Opcional.                                                                                                                                              |
| [FECHA DE \_ MODIFICACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Se recomienda su uso.                                                                                                                                           |
| [FECHA DE \_ CREACIÓN DEL OBJETO \_ \_ WPD](object-properties.md)                                         | Opcional.                                                                                                                                              |
| [REFERENCIAS ATRÁS DE \_ OBJETOS WPD \_ \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                                                                             |
| [IDENTIFICADOR DE OBJETO \_ FUNCIONAL DEL CONTENEDOR DE OBJETOS \_ \_ \_ \_ WPD](object-properties.md)     | Opcional.                                                                                                                                              |
| [OBJETO WPD \_ \_ GENERACIÓN \_ DE \_ MINIATURAS A PARTIR DEL \_ RECURSO](object-properties.md) | Opcional.                                                                                                                                              |
| [EL OBJETO \_ WPD \_ PUEDE \_ ELIMINAR](object-properties.md)                                                                     | Obligatorio si no se puede eliminar el objeto.                                                                                                              |
| [CONFIGURACIÓN REGIONAL DEL \_ \_ LENGUAJE DE OBJETOS \_ WPD](object-properties.md)                                                                | Opcional.                                                                                                                                              |
| [CATEGORÍA DE OBJETOS \_ \_ FUNCIONALES DE \_ WPD](miscellaneous-properties.md)                      | Necesario. Vea WPD CONTENT TYPE FUNCTIONAL OBJECT (OBJETO FUNCIONAL DE TIPO DE CONTENIDO [**\_ DE \_ \_ \_ WPD)**](wpd-content-type-functional-object.md) para ver las categorías definidas Windows dispositivos portátiles. |
| [TIPO DE \_ ALMACENAMIENTO \_ WPD](storage-properties.md)                                                         | Necesario.                                                                                                                                              |
| [TIPO DE \_ SISTEMA DE ARCHIVOS DE ALMACENAMIENTO \_ \_ \_ WPD](storage-properties.md)                               | Opcional.                                                                                                                                              |
| [CAPACIDAD DE \_ ALMACENAMIENTO DE \_ WPD](storage-properties.md)                                                 | Necesario.                                                                                                                                              |
| [ESPACIO LIBRE \_ DE ALMACENAMIENTO \_ WPD EN \_ \_ \_ BYTES](storage-properties.md)                        | Opcional.                                                                                                                                              |
| [ESPACIO LIBRE DE ALMACENAMIENTO DE WPD \_ \_ EN \_ \_ \_ OBJETOS](storage-properties.md)                    | Opcional.                                                                                                                                              |
| [DESCRIPCIÓN DEL \_ ALMACENAMIENTO DE \_ WPD](storage-properties.md)                                           | Opcional.                                                                                                                                              |
| [NÚMERO DE SERIE \_ DE ALMACENAMIENTO \_ DE \_ WPD](storage-properties.md)                                      | Opcional.                                                                                                                                              |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                    | Obligatorio u opcional | Descripción                                        |
|--------------------------------------------------|----------------------|----------------------------------------------------|
| [**ICONO DE RECURSO \_ DE \_ WPD**](wpd-resource-icon.md) | Opcional.            | Contiene la representación del icono para este almacenamiento. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**OBJETO FUNCIONAL \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD**](wpd-content-type-functional-object.md)
</dt> </dl>

 

 



