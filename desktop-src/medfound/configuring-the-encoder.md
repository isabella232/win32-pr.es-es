---
description: Propiedades de codificación
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: Propiedades de codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc7a1528e68153c742ece8c8d7fcb34bfb9b7bbc08f86567f51b54754bb6da3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743497"
---
# <a name="encoding-properties"></a>Propiedades de codificación

Los Windows Media Audio y Windows Media Video admiten diversos modos de codificación. Por lo general, estos modos se configuran estableciendo propiedades en el codificador [Media Foundation transformación](media-foundation-transforms.md) (MFT). Para realizar la codificación de archivos, ya sea mediante componentes de nivel WMContainer o mediante la creación de una topología parcial, debe configurar el codificador correctamente estableciendo propiedades en función del modo de codificación y el tipo de medio de la secuencia. Debe establecerse el mismo conjunto de propiedades tanto en el codificador como en el objeto (receptor de archivos ASF o multiplexor de ASF) que se usa para escribir el archivo ASF.

Las propiedades del codificador se definen en wmcodecdsp.h. Las propiedades específicas que se usan para configurar el codificador se establecen mediante los métodos de la [**interfaz IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

-   [Propiedades de secuencia de audio](#audio-stream-properties)
-   [Propiedades de Secuencia de vídeo](#video-stream-properties)
-   [Configuración de la configuración del Almacén de propiedades](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a>Propiedades de secuencia de audio

En la tabla siguiente se muestran las configuraciones del codificador para una secuencia de audio.



| Tipo de codificación                                                                                        | Nombre de propiedad: valor                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificación de velocidad de bits constante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED - **FALSE** (opcional)De forma predeterminada, MFPKEY \_ VBRENABLED se establece en **FALSE.**<br/>                                                                                             |
| [Codificación de velocidad de bits variable basada en la calidad](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED: **TRUE**<br/> MFPKEY \_ PASSESUSED - 1 (opcional)<br/> De forma predeterminada, MFPKEY \_ PASSESUSED está establecido en 1.<br/> MFPKEY \_ DESIRED \_ VBRQUALITY: de 0 a 100<br/> |
| [Codificación de velocidad de bits variable sin restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED: **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/>                                                                                                                          |
| [Codificación de velocidad de bits variable limitada máxima](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED: **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/> MFPKEY \_ RMAX: velocidad de bits máxima<br/> MFPKEY \_ BMAX: ventana de búfer máxima<br/>                               |



 

### <a name="video-stream-properties"></a>Propiedades de Secuencia de vídeo

En la tabla siguiente se muestran las configuraciones del codificador para una secuencia de vídeo.



| Tipo de codificación                                                                                        | Nombre de propiedad                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codificación de velocidad de bits constante](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED - **FALSE** (opcional)<br/> De forma predeterminada, MFPKEY \_ VBRENABLED se establece en **FALSE.**<br/> MFPKEY \_ VIDEOWINDOW: ventana Búfer<br/>                                  |
| [Codificación de velocidad de bits variable basada en la calidad](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED: **TRUE**<br/> MFPKEY \_ PASSESUSED - 1 (opcional)<br/> De forma predeterminada, MFPKEY \_ PASSESUSED está establecido en 1.<br/> MFPKEY \_ DESIRED \_ VBRQUALITY: de 0 a 100<br/> |
| [Codificación de velocidad de bits variable sin restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED: **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/>                                                                                                                          |
| [Codificación de velocidad de bits variable limitada máxima](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED: **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/> MFPKEY \_ RMAX: velocidad de bits máxima<br/> MFPKEY \_ BMAX: ventana de búfer máxima<br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a>Configuración de la configuración del Almacén de propiedades

Debe configurar un codificador especificando el tipo de codificación y las distintas opciones específicas del flujo antes de la sesión de codificación. También debe establecer las propiedades del codificador en el almacén de propiedades de un objeto ContentInfo de [ASF](asf-contentinfo-object.md) que representa el objeto de encabezado ASF del archivo de salida.

Si usa un MFT de codificador:

1.  Obtenga una referencia a la interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del codificador MFT como se describe en Uso de [la interfaz DETRANSFORM del codificador.](using-an-encoder-s-imftransform--interface.md)
2.  Consulta del MFT del codificador para la **interfaz IPropertyStore.**
3.  Establecer las propiedades necesarias mediante una llamada **a IPropertyStore::SetValue**.

Si usa los objetos de activación del codificador integrados y ya ha creado un receptor de archivos ASF configurado, puede pasar el almacén de propiedades del receptor de medios de ASF a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). El codificador se configura automáticamente en función de la configuración especificada por la aplicación. Para obtener más información, vea el procedimiento descrito en [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).

Para obtener más información sobre cómo crear Media Foundation mediante objetos de activación, vea [Activation Objects](activation-objects.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de instancias de un MFT de codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores multimedia](windows-media-encoders.md)
</dt> </dl>

 

 
