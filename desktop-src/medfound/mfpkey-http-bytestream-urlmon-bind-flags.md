---
description: Establece las marcas de enlace del moniker para la secuencia de bytes HTTP Microsoft Media Foundation.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: Propiedad MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699317"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a>MFPKEY \_ http \_ ByteStream \_ \_ propiedad flags de enlace de urlmon \_

Establece las marcas de enlace del moniker para la secuencia de bytes HTTP Microsoft Media Foundation.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Observaciones

Utilice esta propiedad para configurar la secuencia de bytes HTTP Media Foundation. Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

El valor de esta propiedad es **una operación OR bit a bit** de las marcas de la enumeración **BINDF** . Esta propiedad solo se aplica cuando la propiedad [MFPKEY \_ http \_ ByteStream \_ enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) está establecida en **Variant \_ true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
