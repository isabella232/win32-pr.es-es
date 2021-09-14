---
description: Establece las marcas de enlace del moniker para la Microsoft Media Foundation de bytes HTTP.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268999"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a>Propiedad MFPKEY \_ HTTP \_ ByteStream \_ Urlmon \_ Bind \_ Flags

Establece las marcas de enlace del moniker para la Microsoft Media Foundation de bytes HTTP.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Observaciones

Use esta propiedad para configurar el flujo Media Foundation de bytes HTTP. Para establecer la propiedad , pase un [**puntero IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

El valor de esta propiedad es un **OR** bit a bit de marcas de la **enumeración BINDF.** Esta propiedad solo se aplica cuando la propiedad [ \_ MFPKEY HTTP \_ ByteStream Enable \_ \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) está establecida en **VARIANT \_ TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
