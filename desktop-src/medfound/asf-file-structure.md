---
description: En este tema se describe la estructura de un archivo de formato de sistemas avanzados (ASF).
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Estructura de archivos asf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80dd154978f3796236cd39c0db6743101da8099b695096d375d9214d0bcec799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881236"
---
# <a name="asf-file-structure"></a>Estructura de archivos asf

En este tema se describe la estructura de un archivo de formato de sistemas avanzados (ASF).

Para obtener información detallada sobre los archivos ASF, descargue la [especificación de ASF](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea). También puede usar la herramienta [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) para ver la estructura de un archivo ASF existente.

La unidad base de organización para los archivos ASF se denomina *objeto*. Un objeto de archivo ASF contiene los datos siguientes.



| data                                                        | Size     |
|-------------------------------------------------------------|----------|
| GUID que identifica el objeto.                          | 128 bits |
| El tamaño del objeto.                                     | 64 bits. |
| Datos de objeto. Los datos del objeto pueden contener otros objetos ASF. | Varía.  |



 

> [!Note]  
> Un objeto de archivo ASF es simplemente un fragmento de datos. No es un objeto en el sentido de programación del equipo.

 

Un archivo ASF contiene tres tipos de objetos de archivo de nivel superior.



| Objeto de archivo ASF                                                                                                                      | Descripción                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Objeto de encabezado<br/>         | Contiene información sobre el archivo ASF.<br/>  |
| <span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Objeto de datos<br/>                     | Contiene paquetes de datos multimedia.<br/>           |
| <span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Objetos de índice<br/> | Contiene uno o varios índices. (Opcional).<br/> |



 

En el diagrama siguiente se muestra la estructura de archivos de ASF.

![diagrama que muestra la estructura de archivos asf, incluidos los elementos del encabezado, los datos y el índice](images/asf-components04.png)

Este diagrama no se dibuja para escalar; normalmente, el objeto de datos consta de la mayor parte del archivo.

### <a name="header-object"></a>Objeto de encabezado

El objeto de encabezado es obligatorio y aparece al principio de cada archivo ASF. Contiene atributos de archivo globales e información sobre las secuencias del archivo ASF. Esta información se usa para interpretar y reproducir los datos del archivo.

El objeto header contiene varios subelementos madatory:

-   El objeto De propiedades de archivo describe los atributos globales del archivo, como el tamaño del archivo, la duración de reproducción, el número de paquetes de datos, el tamaño mínimo y máximo de paquetes y la velocidad de bits máxima.
-   El objeto de extensión de encabezado permite agregar funcionalidad adicional a un archivo ASF mientras se mantiene la compatibilidad con versiones anteriores.
-   El objeto Propiedades de secuencia describe una secuencia del archivo. Un archivo ASF debe contener al menos una secuencia y, por tanto, al menos un objeto de propiedades de secuencia.

El objeto de encabezado puede contener información opcional adicional, incluidos los metadatos sobre el archivo (como el título y el autor), una lista de los códecs usados para codificar el archivo y la información de protección de contenido.

### <a name="data-object"></a>Objetos de datos

El objeto de datos de ASF contiene todos los datos multimedia del archivo ASF. Este objeto es obligatorio y debe seguir el objeto de encabezado de ASF.

El objeto de datos se divide en paquetes de *datos.* Cada paquete contiene datos para una o varias secuencias del archivo. Un paquete de datos contiene un encabezado de paquete de datos que proporciona información de análisis de paquetes, seguido de los datos de carga útil de los datos multimedia digitales reales. Todos los paquetes de datos tienen un tiempo de presentación asociado y se organizan en el orden recibido.

La información sobre el contenido del objeto de datos, como el tamaño del paquete y el número de paquetes, se almacena en el objeto de encabezado.

### <a name="index-object"></a>Index (objeto)

El objeto index es opcional y es el último objeto del archivo ASF. Un archivo ASF puede contener más de un objeto index. El objeto index proporciona acceso aleatorio basado en el tiempo al objeto de datos de ASF.

Un objeto de índice simple es otro tipo de índice.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




