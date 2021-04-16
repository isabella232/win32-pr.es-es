---
description: Habilita el Microsoft Media Foundation secuencia de bytes HTTP para usar monikers de dirección URL (también denominado urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: Propiedad MFPKEY_HTTP_ByteStream_Enable_Urlmon (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679109"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>MFPKEY \_ http \_ ByteStream \_ habilitar \_ propiedad de urlmon

Habilita el Microsoft Media Foundation secuencia de bytes HTTP para usar monikers de dirección URL (también denominado *urlmon*).



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**VARIANTE \_ bool**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Observaciones

Utilice esta propiedad para configurar la secuencia de bytes HTTP Media Foundation. Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

Si el valor es **Variant \_ true**, el flujo de bytes http usa urlmon para el transporte http. De lo contrario, si el valor es **Variant \_ false**, el flujo de bytes usa winhttp.

El valor predeterminado es **Variant \_ true** para las aplicaciones de la tienda Windows y **Variant \_ false** para la aplicación de escritorio de Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
