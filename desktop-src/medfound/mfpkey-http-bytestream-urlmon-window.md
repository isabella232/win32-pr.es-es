---
description: Establece una ventana para el Microsoft Media Foundation de bytes HTTP.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: MFPKEY_HTTP_ByteStream_Urlmon_Window propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474097"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a>Propiedad MFPKEY \_ HTTP \_ ByteStream \_ Urlmon \_ Window

Establece una ventana para el Microsoft Media Foundation de bytes HTTP. La ventana se usa para presentar información en la interfaz de usuario durante una operación de enlace.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**IUnknown\***

VT \_ UNKNOWN

**yaldaVal**



## <a name="remarks"></a>Observaciones

Use esta propiedad para configurar el flujo Media Foundation de bytes HTTP. Para establecer la propiedad , pase un [**puntero IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

El valor de esta propiedad es un puntero a la **interfaz IWindowForBindingUI.** Esta propiedad solo se aplica cuando la propiedad [ \_ MFPKEY HTTP \_ ByteStream Enable \_ \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) está establecida en **VARIANT \_ TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
