---
description: Establece la tolerancia, en milisegundos, que se utiliza cuando el origen de medios ASF realiza búsquedas iterativas.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: Propiedad MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697952"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ tolerancia \_ en \_ milisegundos

Establece la tolerancia, en milisegundos, que se utiliza cuando el origen de medios ASF realiza búsquedas iterativas.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Observaciones

Utilice esta propiedad para configurar el origen de medios ASF. Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

Esta propiedad solo se aplica cuando está habilitada la búsqueda iterativa. Para obtener más información, consulte [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

El algoritmo de búsqueda iterativa se detiene si encuentra un paquete cuya distancia desde el tiempo de búsqueda está dentro de la tolerancia especificada. El valor predeterminado es 8000 milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




