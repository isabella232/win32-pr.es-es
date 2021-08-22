---
description: Permite que la Microsoft Media Foundation de bytes HTTP use monikers de dirección URL (también denominado Urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: MFPKEY_HTTP_ByteStream_Enable_Urlmon propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ede2b9109a7345f3a0d764f6a8fa68952686c5ca05207d01bb0a2e54cea4d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344385"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>Propiedad MFPKEY \_ HTTP \_ ByteStream \_ Enable \_ Urlmon

Permite que Microsoft Media Foundation flujo de bytes HTTP use monikers de dirección URL (también denominado *Urlmon).*



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Comentarios

Use esta propiedad para configurar el flujo Media Foundation de bytes HTTP. Para establecer la propiedad , pase un [**puntero IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

Si el valor es **VARIANT \_ TRUE,** la secuencia de bytes HTTP usa Urlmon para el transporte HTTP. De lo contrario, si el valor es **VARIANT \_ FALSE,** la secuencia de bytes usa WinHTTP.

El valor predeterminado es **VARIANT \_ TRUE para las** aplicaciones Windows Store y VARIANT **\_ FALSE** para Windows de escritorio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
