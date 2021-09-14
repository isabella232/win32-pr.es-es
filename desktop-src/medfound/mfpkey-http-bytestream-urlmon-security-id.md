---
description: Establece el identificador de seguridad raíz para la Microsoft Media Foundation de bytes HTTP.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: MFPKEY_HTTP_ByteStream_Urlmon_Security_Id propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363831"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
