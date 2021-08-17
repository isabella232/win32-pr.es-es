---
description: Indica que moov se escribirá antes del cuadro mdat en el archivo generado.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: MF_MPEG4SINK_MOOV_BEFORE_MDAT atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98614484beee5187364570e3c5517ba0f61e0d77161484b59af93a9f5a6512c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104741"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>Atributo \_ MOOV MF MPEG4SINK \_ BEFORE \_ \_ MDAT

Indica que "moov" se escribirá antes del cuadro "mdat" en el archivo generado.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El comportamiento predeterminado del receptor multimedia mpeg4 es escribir "moov" después del cuadro "mdat". Al establecer este atributo, el archivo generado escribe "moov" antes del cuadro "mdat".

Para que el receptor mpeg4 use este atributo, la secuencia de bytes que se pasa no debe ser de búsqueda lenta ni remota para .

Esta característica implica una copia o reuxación de archivos adicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 




