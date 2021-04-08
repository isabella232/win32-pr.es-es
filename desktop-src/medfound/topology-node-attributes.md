---
description: Atributos de nodo de topología
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Atributos de nodo de topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001583"
---
# <a name="topology-node-attributes"></a>Atributos de nodo de topología

Los siguientes atributos se aplican a los nodos de la topología.

## <a name="general-topology-node-attributes"></a>Atributos de nodo de topología general



| Atributo                                                                       | Descripción                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_método de \_ conexión MF TOPONODE \_**](mf-toponode-connect-method-attribute.md)   | Especifica cómo el cargador de topología conecta este nodo de topología y si este nodo es opcional.                                                        |
| [**descodificador de MF \_ TOPONODE \_**](mf-toponode-decoder-attribute.md)                  | Especifica si el objeto de un nodo topología es un descodificador.                                                                                                  |
| [**\_DEScifrador MF TOPONODE \_**](mf-toponode-decryptor-attribute.md)              | Especifica si el objeto subyacente de un nodo topología es un descifrador.                                                                                     |
| [**MF \_ TOPONODE \_ descartable**](mf-toponode-discardable-attribute.md)          | Especifica si la canalización puede quitar ejemplos de un nodo de topología.                                                                                    |
| [**\_MAJORTYPE TOPONODE \_ error de MF \_**](mf-toponode-error-majortype-attribute.md) | Contiene el tipo de medio principal para un nodo de topología. Este atributo se establece cuando no se puede cargar la topología porque no se pudo encontrar el descodificador correcto. |
| [**subtipo de \_ error MF TOPONODE \_ \_**](mf-toponode-error-subtype-attribute.md)     | Contiene el subtipo de medio para un nodo de topología. Este atributo se establece cuando no se puede cargar la topología porque no se pudo encontrar el descodificador correcto.    |
| [**\_código de \_ ERRORCODE TOPONODE MF**](mf-toponode-errorcode-attribute.md)              | Contiene el código de error del error de conexión más reciente para este nodo de topología.                                                                  |
| [**MF \_ TOPONODE \_ bloqueado**](mf-toponode-locked-attribute.md)                    | Especifica si los tipos de medios se pueden cambiar en este nodo de topología.                                                                                  |
| [**\_TOPONODE MF \_ \_ aquí**](mf-toponode-markin-here-attribute.md)         | Especifica si la canalización aplica el marcado en este nodo.                                                                                             |
| [**MF \_ TOPONODE \_ MARKOUT \_ aquí**](mf-toponode-markout-here-attribute.md)       | Especifica si la canalización aplica el marcado en este nodo.                                                                                            |



 

## <a name="source-node-attributes"></a>Atributos del nodo de origen



| Atributo                                                                                       | Descripción                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)                            | Especifica la hora de inicio de una presentación, relativa al inicio del archivo de origen multimedia, en unidades de 100-nanosegundos. |
| [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)                              | Especifica la hora de detención de una presentación, relativa al inicio del archivo de origen multimedia, en unidades de 100-nanosegundos.  |
| [**descriptor de presentación de MF \_ TOPONODE \_ \_**](mf-toponode-presentation-descriptor-attribute.md) | Contiene un puntero al descriptor de presentación para el origen de medios.                                           |
| [**MF \_ TOPONODE \_ Sequence \_ ELEMENTID**](mf-toponode-sequence-elementid-attribute.md)           | Especifica el elemento que contiene un nodo de origen.                                                                |
| [**origen de MF \_ TOPONODE \_**](mf-toponode-source-attribute.md)                                    | Contiene un puntero al origen multimedia asociado a un nodo de topología.                                           |
| [**descriptor de secuencia MF \_ TOPONODE \_ \_**](mf-toponode-stream-descriptor-attribute.md)             | Contiene un puntero al descriptor de flujo para el origen de medios.                                                 |
| [**identificador de WORKQUEUE de MF \_ TOPONODE \_ \_**](mf-toponode-workqueue-id-attribute.md)                       | Especifica una cola de trabajo para un nodo de topología.                                                                       |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS ( \_ clase)**](mf-toponode-workqueue-mmcss-class-attribute.md)    | Especifica una tarea del servicio de programador de clases multimedia (MMCSS) para un nodo de topología.                                  |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | Especifica un identificador de la tarea MMCSS para un nodo de topología.                                                            |



 

## <a name="transform-node-attributes"></a>Transformación de atributos de nodo



| Atributo                                                                             | Descripción                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ D3DAWARE**](mf-toponode-d3daware-attribute.md)                      | Especifica si la transformación asociada a un nodo de topología es compatible con la aceleración de vídeo de DirectX (DXVA) |
| [**\_desagüe TOPONODE \_**](mf-toponode-drain-attribute.md)                            | Especifica cuándo se purga una transformación.                                                                     |
| [**\_vaciado de TOPONODE MF \_**](mf-toponode-flush-attribute.md)                            | Especifica cuándo se vacía una transformación.                                                                     |
| [**MF \_ TOPONODE \_ Transform \_ objectId**](mf-toponode-transform-objectid-attribute.md) | Identificador de clase (CLSID) de la transformación asociada a este nodo de topología.                          |



 

## <a name="output-node-attributes"></a>Atributos del nodo de salida



| Atributo                                                                                  | Descripción                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ deshabilitar \_ preroll**](mf-toponode-disable-preroll-attribute.md)            | Especifica si la sesión multimedia utiliza el preparado en el receptor de medios representado por este nodo de topología.            |
| [**MF \_ TOPONODE \_ noshutdown \_ al \_ quitar**](mf-toponode-noshutdown-on-remove-attribute.md) | Especifica si la sesión multimedia apaga el receptor de medios cuando el nodo de salida se quita de la topología. |
| [**MF \_ TOPONODE sin \_ velocidad**](mf-toponode-rateless-attribute.md)                           | Especifica si el receptor de medios asociado a este nodo de topología tiene un número inestable.                                 |
| [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md)                           | El identificador de flujo del receptor de flujo asociado a este nodo de topología.                                     |



 

## <a name="tee-node-attributes"></a>Tee (atributos de nodo)



| Atributo                                                                  | Descripción                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [**MF \_ TOPONODE \_ PRIMARYOUTPUT**](mf-toponode-primaryoutput-attribute.md) | Indica qué salida es la salida principal en un nodo tee. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 



