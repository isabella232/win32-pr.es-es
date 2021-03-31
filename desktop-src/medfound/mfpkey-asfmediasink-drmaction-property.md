---
description: Especifica cómo el receptor de medios ASF debe aplicar DRM de Windows Media.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: Propiedad MFPKEY_ASFMEDIASINK_DRMACTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820327"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>\_ \_ Propiedad DRMACTION de MFPKEY ASFMEDIASINK

Especifica cómo el receptor de medios ASF debe aplicar DRM de Windows Media.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Observaciones

El valor de esta propiedad es un miembro de la enumeración [**MFSINK \_ WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) .

Puede utilizar este atributo para configurar el receptor de medios ASF. El uso depende de la función a la que llame para crear el receptor de medios ASF:

-   [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Consulte el puntero [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para la interfaz **IPropertyStore** .

-   [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): llame a [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) en el puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado en el parámetro *pContentInfo* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
