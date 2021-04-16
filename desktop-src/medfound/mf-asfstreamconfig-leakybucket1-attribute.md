---
description: Establece el promedio &\# 0034; depósito de fugas&\# 0034; parámetros (vea la sección comentarios) para codificar un archivo de Windows Media. Establezca este atributo mediante la interfaz IMFASFStreamConfig.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET1 atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696764"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a>\_ \_ Atributo LEAKYBUCKET1 de MF ASFSTREAMCONFIG

Establece el promedio de parámetros de "depósito de fugas" (vea la sección comentarios) para codificar un archivo de Windows Media. Establezca este atributo mediante la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

El valor de este atributo es una matriz de tres **DWORD** s, en el orden siguiente:

-   Velocidad de bits, en bits por segundo.
-   Ventana de búfer, en milisegundos.
-   Llenado inicial del búfer, en bytes.

Para obtener más información sobre el concepto de depósito con fugas, vea el tema [modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md) en la documentación del SDK de Windows Media Format.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




