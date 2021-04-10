---
description: Divisor ASF
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: Divisor ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153689"
---
# <a name="asf-splitter"></a>Divisor ASF

El objeto de *separador* ASF es un componente de nivel WMContainer que analiza el objeto de datos ASF de un archivo de formato de sistema avanzado (ASF). Puede usar el divisor para leer los paquetes de datos en el objeto de datos y generar ejemplos de secuencias. Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).

El divisor expone la interfaz [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) . El divisor analiza los paquetes de datos ASF de las secuencias seleccionadas y los vuelve a empaquetar en objetos de ejemplo individuales que exponen la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) . El divisor es uno de los componentes de nivel de plataforma de Media Foundation. El origen de medios ASF usa el divisor internamente para analizar archivos ASF.

En el siguiente diagrama se ilustra la generación de muestras para un archivo ASF a través del divisor.

![diagrama que muestra la generación de ejemplo de un archivo ASF](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

Esta sección contiene los siguientes temas:



| Tema                                                                                                                        | Descripción                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Crear el objeto divisor de ASF](creating-the-asf-splitter-object.md)                                                     | Cómo crear e inicializar el divisor.                              |
| [Configurar el objeto divisor de ASF](configuring-the-asf-splitter-object.md)                                               | Opciones de configuración para el divisor.                                |
| [Generar ejemplos de secuencia a partir de un objeto de datos ASF existente](generating-stream-samples-from-an-existing-asf-data-object.md) | Cómo analizar el objeto de datos ASF y generar muestras de vapor de paquetes. |



 

En la tabla siguiente se muestran los atributos de objeto de datos pertinentes.



| Atributo                                                                                                    | Descripción                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ paquetes FILEPROPERTIES MF de \_ ASF**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Número de paquetes de datos en el objeto de datos ASF.                                                       |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ min \_ Packet \_ size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Tamaño mínimo de los paquetes de datos en el archivo, en bytes.                                              |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ tamaño máximo de \_ paquete \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Tamaño máximo de los paquetes de datos en el archivo, en bytes                                               |
| [**\_longitud de \_ \_ datos ASF \_ de MF PD**](mf-pd-asf-data-length-attribute.md)                                         | Tamaño del objeto de datos ASF, en bytes.                                                               |
| [**\_desplazamiento de \_ \_ Inicio de datos ASF \_ \_ de MF PD**](mf-pd-asf-data-start-offset-attribute.md)                            | Desplazamiento, en bytes, al primer paquete de datos del objeto de datos ASF relativo al inicio del archivo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de WMContainer ASF](wmcontainer-asf-components.md)
</dt> <dt>

[Tutorial: lectura de un archivo ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



