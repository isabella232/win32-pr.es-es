---
description: Establece el identificador de seguridad raíz para la Microsoft Media Foundation de bytes HTTP.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: MFPKEY_HTTP_ByteStream_Urlmon_Security_Id propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d64b07dc7d419624bfe300b890b58554394a5cd3e8363ddcbc4d5be91d9e4b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738012"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a>Propiedad MFPKEY \_ HTTP \_ ByteStream \_ Urlmon \_ Security \_ Id

Establece el identificador de seguridad raíz para la Microsoft Media Foundation de bytes HTTP.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**CAUB**

VT \_ VECTOR \| VT \_ UI1

**caub**



## <a name="remarks"></a>Observaciones

Use esta propiedad para configurar el flujo Media Foundation de bytes HTTP. Para establecer la propiedad , pase un [**puntero IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

Esta propiedad solo se aplica cuando la propiedad [ \_ MFPKEY HTTP \_ ByteStream Enable \_ \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) está establecida en **VARIANT \_ TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
