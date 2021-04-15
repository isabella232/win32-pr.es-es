---
description: En este tema se describe la estructura de un archivo de formato de sistema avanzado (ASF).
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Estructura de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539657"
---
# <a name="asf-file-structure"></a>Estructura de archivos ASF

En este tema se describe la estructura de un archivo de formato de sistema avanzado (ASF).

Para obtener información detallada acerca de los archivos ASF, descargue la [especificación ASF](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea). También puede usar la herramienta [Windows Media ASF Viewer 9 series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) para ver la estructura de un archivo ASF existente.

La unidad base de la organización para los archivos ASF se denomina *objeto*. Un objeto de archivo ASF contiene los datos siguientes.



| Datos                                                        | Tamaño     |
|-------------------------------------------------------------|----------|
| GUID que identifica el objeto.                          | 128 bits |
| El tamaño del objeto.                                     | 64 bits. |
| Datos de objeto. Los datos del objeto pueden contener otros objetos ASF. | Varía.  |



 

> [!Note]  
> Un objeto de archivo ASF es simplemente un fragmento de datos. No es un objeto en el sentido de la programación del equipo.

 

Un archivo ASF contiene tres tipos de objetos de archivo de nivel superior.



| ASF (objeto de archivo)                                                                                                                      | Descripción                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Objeto de encabezado<br/>         | Contiene información acerca del archivo ASF.<br/>  |
| <span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Objeto de datos<br/>                     | Contiene paquetes de datos multimedia.<br/>           |
| <span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Objeto (s) de índice<br/> | Contiene uno o más índices. (Opcional).<br/> |



 

En el diagrama siguiente se muestra la estructura de archivos ASF.

![diagrama que muestra la estructura de archivos ASF, incluidos los elementos del encabezado, los datos y el índice](images/asf-components04.png)

Este diagrama no se dibuja en la escala; Normalmente, el objeto de datos consta de la mayor parte del archivo.

### <a name="header-object"></a>Objeto de encabezado

El objeto de encabezado es obligatorio y aparece al principio de cada archivo ASF. Contiene atributos de archivo globales e información acerca de las secuencias del archivo ASF. Esta información se usa para interpretar y reproducir los datos en el archivo.

El objeto de encabezado contiene varios subobjetos maalmacén:

-   El objeto de propiedades de archivo describe los atributos globales del archivo, como el tamaño del archivo, la duración de la reproducción, el número de paquetes de datos, el tamaño de paquete mínimo y máximo y la velocidad de bits máxima.
-   El objeto de extensión de encabezado permite agregar funcionalidad adicional a un archivo ASF manteniendo la compatibilidad con versiones anteriores.
-   El objeto Stream Properties describe un flujo en el archivo. Un archivo ASF debe contener al menos un flujo y, por consiguiente, al menos un objeto de propiedades de la secuencia.

El objeto de encabezado puede contener información adicional opcional, incluidos los metadatos sobre el archivo (como el título y el autor), una lista de los códecs que se usan para codificar el archivo y la información de protección del contenido.

### <a name="data-object"></a>Objetos de datos

El objeto de datos ASF contiene todos los datos multimedia del archivo ASF. Este objeto es obligatorio y debe seguir el objeto de encabezado ASF.

El objeto de datos se divide en *paquetes* de datos. Cada paquete contiene datos de una o varias secuencias del archivo. Un paquete de datos contiene un encabezado de paquete de datos que proporciona información de análisis de paquetes, seguida de los datos de carga de los datos multimedia digitales reales. Todos los paquetes de datos tienen un tiempo de presentación asociado a él y se organizan en el orden recibido.

La información sobre el contenido del objeto de datos, como el tamaño de paquete y el número de paquetes, se almacena en el objeto de encabezado.

### <a name="index-object"></a>Index (objeto)

El objeto index es opcional y es el último objeto del archivo ASF. Un archivo ASF puede contener más de un objeto de índice. El objeto index proporciona acceso aleatorio basado en el tiempo en el objeto de datos ASF.

Un objeto de índice simple es otro tipo de índice.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




