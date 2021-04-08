---
description: Algunos codificadores de Windows Media y Media Foundation en el nivel de canalización admiten los modos de codificación de dos pasos.
ms.assetid: 3fd5baff-142f-453e-bb97-b355ee6678fc
title: Cómo crear una topología para Two-Pass la codificación de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c813b9a3c31fafaa3efbea83180c997bc46079d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003349"
---
# <a name="how-to-create-a-topology-for-two-pass-windows-media-encoding"></a>Cómo crear una topología para Two-Pass la codificación de Windows Media

Algunos codificadores de Windows Media y Media Foundation en el nivel de canalización admiten los modos de codificación de dos pasos. La aplicación debe configurar y configurar la topología de codificación similar a la de la codificación de un solo paso, pero en el modo de codificación de dos pasos, la aplicación debe ejecutar dos veces la sesión de codificación. En el primer paso, el codificador recopila información sobre el contenido de la secuencia. En el segundo paso, con la información recopilada en el primer paso, se genera el archivo de salida final. Al procesar dos veces los ejemplos de la secuencia, la codificación de dos pasos optimiza el proceso de codificación y genera archivos codificados de mayor calidad. Los modos de codificación de dos pasos no se pueden usar en secuencias en directo.

Media Foundation admite los siguientes modos de codificación de dos pasos:

-   [Codificación de velocidad de bits variable sin restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)
-   [Codificación de velocidad de bits variable máxima limitada](peak-constrained-variable-bit-rate--vbr--encoding.md)

La creación de una topología de codificación para la codificación de dos pasos es similar a la de los modos de paso único. En la lista siguiente se muestran las diferencias clave.

-   La configuración del codificador debe incluir la propiedad [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md) establecida en 2 y la propiedad [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en Variant \_ true. Esto filtra las capacidades del codificador para los modos de dos pasos. Si usa objetos de activación, pase estas propiedades a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).
-   En el primer paso, utilice un receptor de medios ficticios en el nodo de salida, ya que los ejemplos que se generan en este paso no se agregan al archivo final.
-   En el segundo paso, realice una consulta al codificador para las propiedades posteriores a la codificación y reemplace el nodo del receptor multimedia ficticio por el receptor de medios ASF con estas propiedades establecidas.

Para obtener más información acerca de cómo configurar una topología de codificación, vea [Tutorial: codificación de Windows Media de un solo paso](tutorial--1-pass-windows-media-encoding.md).

En el procedimiento siguiente se resumen los pasos para codificar el contenido de Windows Media en un contenedor ASF mediante un modo de codificación de dos pasos.

1.  Cree un origen de medios para el especificado mediante el solucionador de origen.
2.  Enumerar las secuencias en el origen de medios.
3.  Cree el receptor de medios ASF y agregue receptores de secuencia en función de las secuencias del origen de medios que deban codificarse.
4.  Cree el receptor de medios.
5.  Cree los codificadores de Windows Media para las secuencias en el archivo de salida.
6.  Configure los codificadores con las propiedades de codificación de dos pasos.
7.  Cree una topología de codificación parcial conectando el origen, los codificadores y el receptor de medios.
8.  Cree una instancia de la sesión multimedia y establezca la topología en la sesión multimedia.
9.  Ejecute el primer paso de codificación controlando la sesión multimedia y obteniendo todos los eventos pertinentes de la sesión multimedia.
10. Cierre y cierre la sesión de codificación.
11. Consulte las siguientes propiedades en el codificador según el tipo de codificación: 

    | Tipo de codificación                                                                                        | Nombre de propiedad                                                                                                                                                                                                                                                                                                                                                     |
    |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [Codificación de velocidad de bits variable sin restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)       | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)<br/>                                                                                                               |
    | [Codificación de velocidad de bits variable máxima limitada](peak-constrained-variable-bit-rate--vbr--encoding.md) | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)<br/> [**MFPKEY \_ Bmax**](mfpkey-bmaxproperty.md)<br/> [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)<br/> |

    

     

12. Cree el receptor de archivos ASF y agregue los receptores de secuencias necesarios en función de las secuencias que desee incluir en el archivo de salida final.
13. Establezca las propiedades del codificador recuperadas en el paso 11 en el receptor de archivos.
14. Reemplace el receptor de medios del nodo de salida por el receptor de archivos recién creado.
15. Cree una instancia de la sesión multimedia y establezca la topología actualizada en la sesión multimedia.
16. Ejecute el paso de segunda codificación controlando la sesión multimedia y obteniendo todos los eventos pertinentes de la sesión multimedia.
17. Espere a que el evento [MEEndOfPresentation](meendofpresentation.md) de la sesión multimedia y en el controlador de eventos obtenga los valores de propiedad de codificación del codificador y establézcalo en el receptor de archivos. Para obtener más información, vea "actualizar las propiedades de codificación en el receptor de archivos" en [Tutorial: codificación de Windows Media de un solo paso](tutorial--1-pass-windows-media-encoding.md).
18. Cierre y cierre la sesión de codificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> </dl>

 

 




