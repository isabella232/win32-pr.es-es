---
description: Especifica si el lector de origen habilita la aceleración de vídeo directX (DXVA) en el descodificador de vídeo.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: MF_SOURCE_READER_DISABLE_DXVA atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e34f7b0f4ce442931dec06fae4801068df4d7e61894bdbc167c9a823ee1b1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059059"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a>Atributo DISABLE \_ \_ \_ \_ DXVA de MF SOURCE READER

Especifica si el lector [de origen habilita](source-reader.md) la aceleración de vídeo directX (DXVA) en el descodificador de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Este atributo se aplica si se cumplen las condiciones siguientes:

-   El lector de origen descodifica una secuencia de vídeo.
-   El descodificador de vídeo admite la descodificación dxva.
-   La aplicación usa el atributo [MF \_ SOURCE READER \_ \_ D3D \_ MANAGER](mf-source-reader-d3d-manager.md) para establecer el Administrador de dispositivos [Direct3D](direct3d-device-manager.md) en el lector de origen.

Este atributo permite que la aplicación deshabilite DXVA mientras se sigue descodando a superficies de Direct3D.

De forma predeterminada, el lector de origen usa el Administrador de dispositivos [Direct3D](direct3d-device-manager.md) para dos propósitos:

-   Para habilitar la descodificación de DXVA en el descodificador de vídeo.
-   Para asignar superficies de Direct3D para los ejemplos de vídeo.

Si el valor del atributo DISABLE DXVA de MF SOURCE READER es TRUE, el lector de origen deshabilita la decodificación dxVA, aunque todavía usa el Administrador de dispositivos direct3D para asignar \_ \_ \_ \_ superficies de Direct3D.  [](direct3d-device-manager.md)

Si no se establece el atributo [MF \_ SOURCE READER \_ \_ D3D \_ MANAGER,](mf-source-reader-d3d-manager.md) se omite el atributo MF \_ SOURCE READER DISABLE \_ \_ \_ DXVA.

El valor predeterminado de este atributo es **FALSE,** lo que significa que la decodificación de DXVA está habilitada cuando está disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> </dl>

 

 




