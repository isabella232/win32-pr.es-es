---
description: Indica que moov se escribirá antes del cuadro mdat en el archivo generado.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: MF_MPEG4SINK_MOOV_BEFORE_MDAT atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468709"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>Atributo \_ MF MPEG4SINK \_ MOOV BEFORE \_ \_ MDAT

Indica que "moov" se escribirá antes del cuadro "mdat" en el archivo generado.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El comportamiento predeterminado del receptor multimedia mpeg4 es escribir "moov" después del cuadro "mdat". Al establecer este atributo, el archivo generado escribe "moov" antes del cuadro "mdat".

Para que el receptor mpeg4 use este atributo, la secuencia de bytes que se pasa no debe ser de búsqueda lenta ni remota para .

Esta característica implica una copia o reuxing de archivos adicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




