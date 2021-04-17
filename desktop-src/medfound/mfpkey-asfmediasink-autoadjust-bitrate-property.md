---
description: Especifica si el receptor de medios ASF ajusta automáticamente la velocidad de bits.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: Propiedad MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697974"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a>\_ \_ Propiedad autoajuste de \_ velocidad de bits de MFPKEY ASFMEDIASINK

Especifica si el receptor de medios ASF ajusta automáticamente la velocidad de bits.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**VARIANTE \_ bool**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Observaciones

Si el valor de esta propiedad es VARIANT \_ true, el receptor de medios ASF ajusta automáticamente la velocidad de bits del contenido ASF en respuesta a las características de las secuencias que se multiplexan.

Esta propiedad afecta a cómo se comporta el receptor de medios ASF cuando una secuencia desborda los parámetros del "cubo de fugas" del receptor:



| Value              | Comportamiento                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANTE \_ true**  | El receptor de medios ASF ajusta automáticamente la velocidad de bits del contenido ASF en respuesta a las características de las secuencias que se multiplexan. |
| **VARIANTE \_ false** | El receptor de medios ASF usa el valor de velocidad de bits de transmisión proporcionado por la aplicación.                                                                |



 

El valor predeterminado es **Variant \_ false**.

Establezca esta propiedad al configurar el receptor de medios ASF. El uso depende de la función a la que llame para crear el receptor de medios ASF:

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Consulte el puntero [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para la interfaz **IPropertyStore** .

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): llame a [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en el puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado en el parámetro *pContentInfo* .

Establecer esta propiedad en VARIANT \_ true hace que el receptor de medios ASF establezca la marca de **\_ velocidad de \_ \_ bits de autoajuste del multiplexor de MFASF** en el multiplexor ASF. Vea [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).

Para obtener más información sobre el concepto de depósito con fugas, vea el tema sobre el modelo de búfer de depósitos con fugas en la documentación del SDK de Windows Media Format.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




