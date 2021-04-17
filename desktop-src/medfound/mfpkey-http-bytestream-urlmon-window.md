---
description: Establece una ventana para el Microsoft Media Foundation secuencia de bytes HTTP.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: Propiedad MFPKEY_HTTP_ByteStream_Urlmon_Window (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709222"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a>MFPKEY \_ http \_ ByteStream \_ propiedad de la ventana de urlmon \_

Establece una ventana para el Microsoft Media Foundation secuencia de bytes HTTP. La ventana se usa para presentar información en la interfaz de usuario durante una operación de enlace.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**IUnknown\***

VT \_ desconocido

**punkVal**



## <a name="remarks"></a>Observaciones

Utilice esta propiedad para configurar la secuencia de bytes HTTP Media Foundation. Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

El valor de esta propiedad es un puntero a la interfaz **IWindowForBindingUI** . Esta propiedad solo se aplica cuando la propiedad [MFPKEY \_ http \_ ByteStream \_ enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) está establecida en **Variant \_ true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
