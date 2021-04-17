---
description: Especifica si una transformación de Media Foundation basado en hardware (MFT) está conectada a otro MFT basado en hardware.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: MFT_CONNECTED_TO_HW_STREAM atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659833"
---
# <a name="mft_connected_to_hw_stream-attribute"></a>MFT \_ conectado \_ al \_ atributo de flujo de HW \_

Especifica si una transformación de Media Foundation basado en hardware (MFT) está conectada a otro MFT basado en hardware.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Normalmente, las aplicaciones no usan este atributo.

Este atributo se usa con MFTs basados en hardware. Cuando dos MFTs de hardware están conectados en una topología, el cargador de topología establece este atributo en **true** en los objetos siguientes:

-   El flujo de salida del MFT ascendente
-   El flujo de entrada del MFT de nivel inferior.

Para obtener el almacén de atributos para el flujo de salida, el cargador de topología llama a [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) en el MFT ascendente. Para obtener el almacén de atributos para el flujo de entrada, el cargador de topología llama a [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) en el MFT de nivel inferior.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs de hardware](hardware-mfts.md)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 




