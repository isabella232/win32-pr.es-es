---
description: Ciertos codificador Windows es multimedia y Media Foundation admiten los modos de codificación de dos Media Foundation en la capa de canalización.
ms.assetid: 3fd5baff-142f-453e-bb97-b355ee6678fc
title: Cómo crear una topología para la codificación Two-Pass Windows multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525a98faa424371f2d80739e5c68f199cfc7ed6443c25ab3d15b575afdd003e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724885"
---
# <a name="how-to-create-a-topology-for-two-pass-windows-media-encoding"></a>Cómo crear una topología para la codificación Two-Pass Windows multimedia

Ciertos codificador Windows es multimedia y Media Foundation admiten los modos de codificación de dos Media Foundation en la capa de canalización. La aplicación debe configurar y configurar la topología de codificación similar a la de la codificación de paso único, pero en el modo de codificación de dos pases, la aplicación debe ejecutar la sesión de codificación dos veces. En el primer paso, el codificador recopila información sobre el contenido de la secuencia. En el segundo paso, mediante la información recopilada en el primer paso, se genera el archivo de salida final. Al procesar dos veces los ejemplos de la secuencia, la codificación de dos pasos optimiza el proceso de codificación y genera archivos codificados de mayor calidad. Los modos de codificación de dos pases no se pueden usar en secuencias en vivo.

Media Foundation admite los siguientes modos de codificación de dos pasos:

-   [Codificación de velocidad de bits variable sin restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)
-   [Codificación de velocidad de bits variable limitada máxima](peak-constrained-variable-bit-rate--vbr--encoding.md)

La creación de una topología de codificación para la codificación de dos pases es similar a los modos de paso único. En la lista siguiente se muestran las principales diferencias.

-   La configuración del codificador debe incluir la propiedad [**\_ MFPKEY PASSESUSED**](mfpkey-passesusedproperty.md) establecida en 2 y la propiedad [**\_ MFPKEY VBRENABLED**](mfpkey-vbrenabledproperty.md) en VARIANT \_ TRUE. Esto filtra las funcionalidades del codificador a modos de dos pases. Si usa objetos de activación, pase estas propiedades a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).
-   Para el primer paso, use un receptor multimedia ficticio en el nodo de salida porque los ejemplos que se generan en este paso no se agregan al archivo final.
-   Para el segundo paso, consulte el codificador para obtener las propiedades posteriores a la codificación necesarias y reemplace el nodo receptor multimedia ficticio por el receptor de medios de ASF por estas propiedades establecidas.

Para obtener más información sobre cómo configurar una topología de codificación, [vea Tutorial: Single Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).

En el procedimiento siguiente se resumen los pasos para codificar Windows contenido multimedia en un contenedor de ASF mediante un modo de codificación de dos pasos.

1.  Cree un origen de medios para el especificado mediante el solucionador de origen.
2.  Enumerar las secuencias en el origen de medios.
3.  Cree el receptor de medios de ASF y agregue receptores de flujo en función de las secuencias del origen de medios que deba codificarse.
4.  Cree el receptor de medios.
5.  Cree el Windows codificadores multimedia para las secuencias del archivo de salida.
6.  Configure los codificadores con las propiedades de codificación de 2 pases.
7.  Cree una topología de codificación parcial conectando el origen, los codificadores y el receptor multimedia.
8.  Cree una instancia de la sesión multimedia y establezca la topología en la sesión multimedia.
9.  Ejecute el primer paso de codificación controlando la sesión multimedia y obteniendo todos los eventos pertinentes de la sesión multimedia.
10. Cierre y cierre la sesión de codificación.
11. Consulte el codificador para obtener las siguientes propiedades en función del tipo de codificación: 

    | Tipo de codificación                                                                                        | Nombre de propiedad                                                                                                                                                                                                                                                                                                                                                     |
    |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [Codificación de velocidad de bits variable sin restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)       | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ FPSG**](mfpkey-ravgproperty.md)<br/>                                                                                                               |
    | [Codificación de velocidad de bits variable limitada máxima](peak-constrained-variable-bit-rate--vbr--encoding.md) | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ FPSG**](mfpkey-ravgproperty.md)<br/> [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md)<br/> [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)<br/> |

    

     

12. Cree el receptor del archivo ASF y agregue los receptores de flujo necesarios en función de las secuencias que quiera incluir en el archivo de salida final.
13. Establezca las propiedades del codificador recuperadas en el paso 11 en el receptor de archivos.
14. Reemplace el receptor de medios en el nodo de salida por el receptor de archivos recién creado.
15. Cree una instancia de la sesión multimedia y establezca la topología actualizada en la sesión multimedia.
16. Ejecute el segundo paso de codificación controlando la sesión multimedia y obteniendo todos los eventos pertinentes de la sesión multimedia.
17. Espere el [evento MEEndOfPresentation](meendofpresentation.md) de la sesión multimedia y, en el controlador de eventos, obtenga los valores de propiedad de codificación del codificador y estables en el receptor del archivo. Para obtener más información, vea "Actualizar propiedades de codificación en el receptor de archivos" en [Tutorial: Single Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).
18. Cierre y cierre la sesión de codificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> </dl>

 

 




