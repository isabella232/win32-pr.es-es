---
description: Atributos de nodo de topología
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Atributos de nodo de topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268716"
---
# <a name="topology-node-attributes"></a>Atributos de nodo de topología

Los siguientes atributos se aplican a los nodos de topología.

## <a name="general-topology-node-attributes"></a>Atributos de nodo de topología general



| Atributo                                                                       | Descripción                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MÉTODO MF \_ TOPONODE \_ \_ CONNECT**](mf-toponode-connect-method-attribute.md)   | Especifica cómo el cargador de topologías conecta este nodo de topología y si este nodo es opcional.                                                        |
| [**DESCODIFICADOR \_ TOPONODE DE MF \_**](mf-toponode-decoder-attribute.md)                  | Especifica si el objeto de un nodo de topología es un descodificador.                                                                                                  |
| [**DESCIFRADOR \_ TOPONODE DE MF \_**](mf-toponode-decryptor-attribute.md)              | Especifica si el objeto subyacente de un nodo de topología es un descifrador.                                                                                     |
| [**MF \_ TOPONODE \_ DISCARDABLE**](mf-toponode-discardable-attribute.md)          | Especifica si la canalización puede quitar muestras de un nodo de topología.                                                                                    |
| [**MF \_ TOPONODE \_ ERROR \_ MAJORTYPE**](mf-toponode-error-majortype-attribute.md) | Contiene el tipo de medio principal para un nodo de topología. Este atributo se establece cuando la topología no se puede cargar porque no se encontró el descodificador correcto. |
| [**SUBTIPO \_ DE ERROR MF TOPONODE \_ \_**](mf-toponode-error-subtype-attribute.md)     | Contiene el subtipo de medio para un nodo de topología. Este atributo se establece cuando la topología no se puede cargar porque no se encontró el descodificador correcto.    |
| [**MF \_ TOPONODE \_ ERRORCODE**](mf-toponode-errorcode-attribute.md)              | Contiene el código de error del error de conexión más reciente para este nodo de topología.                                                                  |
| [**MF \_ TOPONODE \_ LOCKED**](mf-toponode-locked-attribute.md)                    | Especifica si los tipos de medios se pueden cambiar en este nodo de topología.                                                                                  |
| [**MF \_ TOPONODE \_ MARKIN \_ AQUÍ**](mf-toponode-markin-here-attribute.md)         | Especifica si la canalización aplica el mark-in en este nodo.                                                                                             |
| [**MF \_ TOPONODE \_ MARKOUT \_ AQUÍ**](mf-toponode-markout-here-attribute.md)       | Especifica si la canalización aplica la marca de salida en este nodo.                                                                                            |



 

## <a name="source-node-attributes"></a>Atributos del nodo de origen



| Atributo                                                                                       | Descripción                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)                            | Especifica la hora de inicio de una presentación, en relación con el inicio del archivo de origen multimedia, en unidades de 100 nanosegundos. |
| [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)                              | Especifica el tiempo de detenerse de una presentación, en relación con el inicio del archivo de origen multimedia, en unidades de 100 nanosegundos.  |
| [**\_DESCRIPTOR DE PRESENTACIÓN MF TOPONODE \_ \_**](mf-toponode-presentation-descriptor-attribute.md) | Contiene un puntero al descriptor de presentación para el origen multimedia.                                           |
| [**MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID**](mf-toponode-sequence-elementid-attribute.md)           | Especifica el elemento que contiene un nodo de origen.                                                                |
| [**MF \_ TOPONODE \_ SOURCE**](mf-toponode-source-attribute.md)                                    | Contiene un puntero al origen de medios asociado a un nodo de topología.                                           |
| [**\_DESCRIPTOR DE FLUJO MF TOPONODE \_ \_**](mf-toponode-stream-descriptor-attribute.md)             | Contiene un puntero al descriptor de secuencia para el origen de medios.                                                 |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ ID**](mf-toponode-workqueue-id-attribute.md)                       | Especifica una cola de trabajo para un nodo de topología.                                                                       |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ (CLASE MMCSS) \_**](mf-toponode-workqueue-mmcss-class-attribute.md)    | Especifica una tarea del Servicio programador de clases multimedia (MMCSS) para un nodo de topología.                                  |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | Especifica un identificador de tarea MMCSS para un nodo de topología.                                                            |



 

## <a name="transform-node-attributes"></a>Transformar atributos de nodo



| Atributo                                                                             | Descripción                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ D3DAWARE**](mf-toponode-d3daware-attribute.md)                      | Especifica si la transformación asociada a un nodo de topología admite la aceleración de vídeo de DirectX (DXVA) |
| [**PURGA \_ DE TOPONODE \_ DE MF**](mf-toponode-drain-attribute.md)                            | Especifica cuándo se purga una transformación.                                                                     |
| [**MF \_ TOPONODE \_ FLUSH**](mf-toponode-flush-attribute.md)                            | Especifica cuándo se vacía una transformación.                                                                     |
| [**MF \_ TOPONODE \_ TRANSFORM \_ OBJECTID**](mf-toponode-transform-objectid-attribute.md) | Identificador de clase (CLSID) de la transformación asociada a este nodo de topología.                          |



 

## <a name="output-node-attributes"></a>Atributos de nodo de salida



| Atributo                                                                                  | Descripción                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ DISABLE \_ PREROLL**](mf-toponode-disable-preroll-attribute.md)            | Especifica si la sesión multimedia usa la inscripción previa en el receptor de medios representado por este nodo de topología.            |
| [**MF \_ TOPONODE \_ NOSHUTDOWN \_ ON \_ REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) | Especifica si la sesión multimedia cierra el receptor de medios cuando se quita el nodo de salida de la topología. |
| [**MF \_ TOPONODE \_ RATELESS**](mf-toponode-rateless-attribute.md)                           | Especifica si el receptor multimedia asociado a este nodo de topología no tiene velocidad.                                 |
| [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md)                           | Identificador de flujo del receptor de flujo asociado a este nodo de topología.                                     |



 

## <a name="tee-node-attributes"></a>Atributos de nodo de tee



| Atributo                                                                  | Descripción                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [**MF \_ TOPONODE \_ PRIMARYOUTPUT**](mf-toponode-primaryoutput-attribute.md) | Indica qué salida es la salida principal en un nodo de tee. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 



