---
description: Divisor de ASF
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: Divisor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac425be62ba7898bd23c41dd69d3b637ccba766b135d1fd200344e4f7ff4e98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881126"
---
# <a name="asf-splitter"></a>Divisor de ASF

El objeto *divisor* ASF es un componente de capa WMContainer que analiza el objeto de datos ASF de un archivo de formato de sistemas avanzados (ASF). Puede usar el divisor para leer los paquetes de datos en el objeto de datos y generar ejemplos de flujo. Para obtener información sobre la estructura de un archivo ASF, vea [ASF File Structure](asf-file-structure.md).

El divisor expone la interfaz [**IMFASFSplitter.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) El divisor analiza los paquetes de datos de ASF para las secuencias seleccionadas y los vuelve a empaquetar en objetos de ejemplo individuales que exponen la [**interfaz DESEJEMPLOEjemplo.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) El divisor es uno de los componentes de nivel de plataforma de Media Foundation. El origen multimedia de ASF usa el divisor internamente para analizar los archivos ASF.

En el diagrama siguiente se muestra la generación de ejemplo para un archivo ASF a través del divisor.

![diagrama que muestra la generación de ejemplo de un archivo asf](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

Esta sección contiene los siguientes temas:



| Tema                                                                                                                        | Descripción                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Creación del objeto divisor de ASF](creating-the-asf-splitter-object.md)                                                     | Cómo crear e inicializar el divisor.                              |
| [Configuración del objeto divisor de ASF](configuring-the-asf-splitter-object.md)                                               | Opciones de configuración para el divisor.                                |
| [Generar ejemplos de flujo a partir de un objeto de datos ASF existente](generating-stream-samples-from-an-existing-asf-data-object.md) | Cómo analizar el objeto de datos de ASF y generar muestras de flujo en paquetes. |



 

En la tabla siguiente se muestran los atributos de objeto de datos pertinentes.



| Atributo                                                                                                    | Descripción                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**PAQUETES \_ \_ FILEPROPERTIES DE ASF DE MF PD \_ \_**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Número de paquetes de datos en el objeto de datos asf.                                                       |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MIN \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Tamaño mínimo de los paquetes de datos del archivo, en bytes.                                              |
| [**ARCHIVO \_ \_ ASF MF \_ PDPROPIEDADES \_ TAMAÑO MÁXIMO DE \_ \_ PAQUETES**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Tamaño máximo de los paquetes de datos del archivo, en bytes                                               |
| [**LONGITUD \_ DE DATOS DE \_ ASF de MF PD \_ \_**](mf-pd-asf-data-length-attribute.md)                                         | Tamaño del objeto de datos asf, en bytes.                                                               |
| [**DESPLAZAMIENTO \_ DE INICIO DE DATOS DE \_ ASF de MF PD \_ \_ \_**](mf-pd-asf-data-start-offset-attribute.md)                            | Desplazamiento, en bytes, al primer paquete de datos del objeto de datos de ASF con respecto al inicio del archivo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de ASF de WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Tutorial: Lectura de un archivo ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



