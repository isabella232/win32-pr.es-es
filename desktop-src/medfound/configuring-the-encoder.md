---
description: Propiedades de codificación
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: Propiedades de codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 093b72dc37501ca88882c6e3b530cda0eed1baa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153665"
---
# <a name="encoding-properties"></a>Propiedades de codificación

Los codificadores Windows Media Audio y Windows Media Video admiten diversos modos de codificación. Estos modos normalmente se configuran mediante el establecimiento de propiedades en el codificador [Media Foundation la transformación](media-foundation-transforms.md) (MFT). Para realizar la codificación de archivos, ya sea mediante el uso de componentes de nivel de WMContainer o mediante la creación de una topología parcial, debe configurar el codificador adecuadamente estableciendo las propiedades en función del modo de codificación y el tipo de medio de la secuencia. El mismo conjunto de propiedades debe establecerse tanto en el codificador como en el objeto (receptor de archivos ASF o multiplexor ASF) que se usa para escribir el archivo ASF.

Las propiedades del codificador se definen en wmcodecdsp. h. Las propiedades específicas que se usan para configurar el codificador se establecen mediante los métodos de la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

-   [Propiedades de secuencia de audio](#audio-stream-properties)
-   [Propiedades de secuencia de vídeo](#video-stream-properties)
-   [Configurar el almacén de propiedades del codificador](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a>Propiedades de secuencia de audio

En la tabla siguiente se muestran las configuraciones del codificador para una secuencia de audio.



| Tipo de codificación                                                                                        | Nombre de propiedad: valor                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificación de velocidad de bits constante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED- **false** (opcional) de forma predeterminada, MFPKEY \_ VBRENABLED está establecido en **false**.<br/>                                                                                             |
| [Codificación de velocidad de bits variable basada en la calidad](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED: **true**<br/> MFPKEY \_ PASSESUSED-1 (opcional)<br/> De forma predeterminada, MFPKEY \_ PASSESUSED se establece en 1.<br/> MFPKEY \_ Desired \_ VBRQUALITY-from 0 to 100<br/> |
| [Codificación de velocidad de bits variable sin restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED: **true**<br/> MFPKEY \_ PASSESUSED-2<br/>                                                                                                                          |
| [Codificación de velocidad de bits variable máxima limitada](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED: **true**<br/> MFPKEY \_ PASSESUSED-2<br/> MFPKEY \_ RMAX-velocidad de bits máxima<br/> MFPKEY \_ Bmax: ventana de búfer máxima<br/>                               |



 

### <a name="video-stream-properties"></a>Propiedades de secuencia de vídeo

En la tabla siguiente se muestran las configuraciones del codificador para una secuencia de vídeo.



| Tipo de codificación                                                                                        | Nombre de propiedad                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificación de velocidad de bits constante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED- **false** (opcional)<br/> De forma predeterminada, MFPKEY \_ VBRENABLED se establece en **false**.<br/> MFPKEY \_ VideoWindow: ventana de búfer<br/>                                  |
| [Codificación de velocidad de bits variable basada en la calidad](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED: **true**<br/> MFPKEY \_ PASSESUSED-1 (opcional)<br/> De forma predeterminada, MFPKEY \_ PASSESUSED se establece en 1.<br/> MFPKEY \_ Desired \_ VBRQUALITY-from 0 to 100<br/> |
| [Codificación de velocidad de bits variable sin restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED: **true**<br/> MFPKEY \_ PASSESUSED-2<br/>                                                                                                                          |
| [Codificación de velocidad de bits variable máxima limitada](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED: **true**<br/> MFPKEY \_ PASSESUSED-2<br/> MFPKEY \_ RMAX-velocidad de bits máxima<br/> MFPKEY \_ Bmax: ventana de búfer máxima<br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a>Configurar el almacén de propiedades del codificador

Debe configurar un codificador especificando el tipo de codificación y los distintos valores específicos de la secuencia antes de la sesión de codificación. También debe establecer las propiedades del codificador en el almacén de propiedades de un [objeto ContentInfo ASF](asf-contentinfo-object.md) que representa el objeto de encabezado ASF del archivo de salida.

Si usa una MFT del codificador:

1.  Obtenga una referencia a la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de la MFT del codificador, tal y como se describe en uso de la [interfaz IMFTransform de un codificador](using-an-encoder-s-imftransform--interface.md).
2.  Consultando la MFT del codificador para la interfaz **IPropertyStore** .
3.  Establecer las propiedades necesarias mediante una llamada a **IPropertyStore:: SetValue**.

Si usa los objetos de activación del codificador integrados y ya ha creado un receptor de archivos ASF, puede pasar el almacén de propiedades del receptor de medios ASF a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). El codificador se configura automáticamente en función de la configuración especificada por la aplicación. Para obtener más información, consulte el procedimiento descrito en el uso de los [objetos de activación de un codificador](using-an-encoder-s-activation-objects.md).

Para obtener más información sobre cómo crear objetos Media Foundation mediante el uso de objetos de activación, vea [objetos de activación](activation-objects.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear instancias de una MFT del codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 
