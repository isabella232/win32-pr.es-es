---
description: Obtiene estadísticas del receptor de medios de la Alianza de redes digitales (DLNA).
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: MF_MP2DLNA_STATISTICS atributo (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544366"
---
# <a name="mf_mp2dlna_statistics-attribute"></a>\_Atributo MF MP2DLNA \_ Statistics

Obtiene estadísticas del receptor de medios de la Alianza de redes digitales (DLNA).

## <a name="data-type"></a>Tipo de datos

**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** almacenado como **byte \[ \]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

## <a name="remarks"></a>Observaciones

Durante el streaming, el receptor de medios DLNA actualiza este atributo con estadísticas sobre la codificación y multiplexación de las secuencias MPEG-2. La aplicación puede consultar este atributo en cualquier momento para obtener los valores más recientes.

Establecer este atributo en el receptor de medios DLNA no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




