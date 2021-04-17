---
description: Establece el identificador de seguridad raíz de la secuencia de bytes HTTP Microsoft Media Foundation.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: Propiedad MFPKEY_HTTP_ByteStream_Urlmon_Security_Id (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700250"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a>MFPKEY \_ http \_ ByteStream \_ urlmon \_ Security \_ ID (propiedad)

Establece el identificador de seguridad raíz de la secuencia de bytes HTTP Microsoft Media Foundation.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**CAUB**

VT \_ Vector \| VT \_ UI1

**caub**



## <a name="remarks"></a>Observaciones

Utilice esta propiedad para configurar la secuencia de bytes HTTP Media Foundation. Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

Esta propiedad solo se aplica cuando la propiedad [MFPKEY \_ http \_ ByteStream \_ enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) está establecida en **Variant \_ true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
