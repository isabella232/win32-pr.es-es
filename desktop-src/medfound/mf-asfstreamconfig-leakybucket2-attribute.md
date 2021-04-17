---
description: Establece el límite máximo &\# 0034; depósito de fugas&\# 0034; parámetros (vea la sección comentarios) para codificar un archivo de Windows Media. Estos parámetros se usan para la velocidad de bits máxima. Establezca este atributo mediante la interfaz IMFASFStreamConfig.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET2 atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678107"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a>\_ \_ Atributo LEAKYBUCKET2 de MF ASFSTREAMCONFIG

Establece los parámetros de límite máximo de "depósito de fugas" (vea la sección comentarios) para codificar un archivo de Windows Media. Estos parámetros se usan para la velocidad de bits máxima. Establezca este atributo mediante la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .

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

[**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




