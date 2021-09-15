---
description: Especifica si se debe incluir un codificador en la topología de transcodificación.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: MF_TRANSCODE_DONOT_INSERT_ENCODER atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468670"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a>Atributo \_ DEL CODIFICADOR MF TRANSCODE \_ DONOT \_ INSERT \_

Especifica si se debe incluir un codificador en la topología de transcodificación.

La [**función MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) comprueba este atributo durante la creación de la topología. Si no se establece este atributo, se inserta un codificador en la topología de transcodificación.

## <a name="data-type"></a>Tipo de datos

**UINT32**



| Value                                                                        | Significado                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Se inserta un codificador en la topología de transcodificación.<br/>                                                      |
| <dl> <dt>1</dt> </dl> | Un codificador no se incluye en la topología de transcodificación. El nodo de origen está conectado al nodo de salida.<br/> |



 

## <a name="remarks"></a>Observaciones

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 




