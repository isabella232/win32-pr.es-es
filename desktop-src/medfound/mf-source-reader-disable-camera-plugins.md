---
description: Deshabilita el uso de complementos de cámara posteriores al procesamiento por el lector de origen.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278922"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a>\_Lector de código fuente MF \_ \_ deshabilitar \_ complemento de cámara ( \_ atributo)

Deshabilita el uso de complementos de cámara posteriores al procesamiento por el [lector de origen](source-reader.md).

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica cuando el lector de origen se usa con un origen de captura de vídeo. Si este atributo es **true**, impide que el lector de código fuente cargue los complementos posteriores al procesamiento que pueda proporcionar la cámara. De lo contrario, de forma predeterminada, el lector de código fuente los cargará.

El valor predeterminado de este atributo es **false**. Establezca el atributo al crear el lector de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del lector de código fuente](source-reader-attributes.md)
</dt> </dl>

 

 




