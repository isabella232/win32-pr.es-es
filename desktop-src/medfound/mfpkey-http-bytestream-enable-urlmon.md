---
description: Permite que el Microsoft Media Foundation de bytes HTTP use monikers de dirección URL (también denominado Urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: MFPKEY_HTTP_ByteStream_Enable_Urlmon propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474098"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>Propiedad MFPKEY \_ HTTP \_ ByteStream \_ Enable \_ Urlmon

Permite que el Microsoft Media Foundation de bytes HTTP use monikers de dirección URL (también denominado *Urlmon).*



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Observaciones

Use esta propiedad para configurar el flujo Media Foundation de bytes HTTP. Para establecer la propiedad , pase un [**puntero IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

Si el valor es **VARIANT \_ TRUE,** la secuencia de bytes HTTP usa Urlmon para el transporte HTTP. De lo contrario, si el valor es **VARIANT \_ FALSE,** la secuencia de bytes usa WinHTTP.

El valor predeterminado es **VARIANT TRUE para \_ las** aplicaciones Windows Store y **VARIANT \_ FALSE** para Windows de escritorio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
