---
description: Permite que el representador de vídeo mejorado (EVR) mejore el rendimiento mediante el desentrelazado de Bob.
ms.assetid: e145e862-b987-4962-a94b-f8370bbcd5ac
title: EVRConfig_AllowDropToBob atributo (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3940edd0945999f7300060d963806e3572a5d0fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423535"
---
# <a name="evrconfig_allowdroptobob-attribute"></a>\_Atributo AllowDropToBob de EVRConfig

Permite que el representador de vídeo mejorado (EVR) mejore el rendimiento mediante el desentrelazado de Bob.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo se puede establecer en el receptor de EVRmedia. Para establecer el atributo, **QueryInterface** para consultar el receptor de medios EVR para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideoMixPrefs \_ ALLOWDROPTOBOB** en EVR. Consulte [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) para obtener una descripción de esta marca.

La constante GUID para este atributo se exporta desde strmiids. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>UUID. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Administración de calidad de vídeo](video-quality-management.md)
</dt> </dl>

 

 




