---
description: Valor del campo &\# 0034;cs(Referer)&0034; que el origen de red usa para el \# registro.
ms.assetid: 328544b3-0d5f-4d1a-9ad1-ac38402d5898
title: MFNETSOURCE_BROWSERWEBPAGE propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e8222761299cad229b692ef400f69d0968ebd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468668"
---
# <a name="mfnetsource_browserwebpage-property"></a>Propiedad MFNETSOURCE \_ BROWSERWEBPAGE

Valor del campo "cs(Referer)" que el origen de red usa para el registro. Las aplicaciones pueden establecer esta propiedad en la dirección URL de la página web en la que se insertó la aplicación.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

Cadena de caracteres anchos (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ BROWSERWEBPAGE** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para configurar el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Registro de cliente](client-logging.md)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




