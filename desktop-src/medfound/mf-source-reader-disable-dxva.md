---
description: Especifica si el lector de origen habilita la aceleración de vídeo DirectX (DXVA) en el descodificador de vídeo.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: MF_SOURCE_READER_DISABLE_DXVA atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361346"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a>\_Lector de origen MF \_ \_ deshabilitar el \_ atributo DXVA

Especifica si el [lector de origen](source-reader.md) habilita la aceleración de vídeo DirectX (DXVA) en el descodificador de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo se aplica si se cumplen las condiciones siguientes:

-   El lector de origen descodifica una secuencia de vídeo.
-   El descodificador de vídeo admite la descodificación de DXVA.
-   La aplicación usa el atributo de [Administrador de D3D de \_ lector de origen \_ \_ \_ MF](mf-source-reader-d3d-manager.md) para establecer la [Administrador de dispositivos de Direct3D](direct3d-device-manager.md) en el lector de origen.

Este atributo permite a la aplicación deshabilitar DXVA mientras se está descodificando en superficies de Direct3D.

De forma predeterminada, el lector de origen usa la [Administrador de dispositivos de Direct3D](direct3d-device-manager.md) para dos propósitos:

-   Para habilitar la descodificación de DXVA en el descodificador de vídeo.
-   Para asignar las superficies de Direct3D para los ejemplos de vídeo.

Si el valor del atributo del \_ lector de código fuente MF \_ \_ deshabilitar el \_ atributo DXVA es **true**, el lector de origen deshabilita la descodificación de DXVA, aunque todavía usa [Direct3D administrador de dispositivos](direct3d-device-manager.md) para asignar las superficies de Direct3D.

Si no se establece el atributo de [ \_ \_ \_ \_ Administrador D3D del lector de origen MF](mf-source-reader-d3d-manager.md) , \_ se omite el atributo del lector de origen MF \_ \_ deshabilitar el \_ atributo DXVA.

El valor predeterminado de este atributo es **false**, lo que significa que la descodificación de DXVA está habilitada cuando está disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Atributos del lector de código fuente](source-reader-attributes.md)
</dt> </dl>

 

 




