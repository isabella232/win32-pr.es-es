---
description: Especifica si un codificador debe estar incluido en la topología de transcodificación.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: MF_TRANSCODE_DONOT_INSERT_ENCODER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696634"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a>MF \_ Transcode \_ donot \_ Insertar \_ atributo Encoder

Especifica si un codificador debe estar incluido en la topología de transcodificación.

La función [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) comprueba este atributo durante la creación de la topología. Si no se establece este atributo, se inserta un codificador en la topología de transcodificación.

## <a name="data-type"></a>Tipo de datos

**UINT32**



| Value                                                                        | Significado                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Se inserta un codificador en la topología de transcodificación.<br/>                                                      |
| <dl> <dt>1</dt> </dl> | Un codificador no se incluye en la topología de transcodificación. El nodo de origen se conecta al nodo de salida.<br/> |



 

## <a name="remarks"></a>Observaciones

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




