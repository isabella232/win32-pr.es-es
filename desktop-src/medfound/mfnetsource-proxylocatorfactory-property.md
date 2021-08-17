---
description: Contiene un puntero a la interfaz IMFNetProxyLocatorFactory.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: MFNETSOURCE_PROXYLOCATORFACTORY propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc06f58fc11e4d0dcff95274170a76b25160b584231bd2c9e39ed1949b1363e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954745"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a>Propiedad MFNETSOURCE \_ PROXYLOCATORFACTORY

Contiene un puntero a la [**interfaz IMFNetProxyLocatorFactory.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory)



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**Puntero IUnknown**

VT \_ UNKNOWN

**yaldaVal**



## <a name="remarks"></a>Comentarios

La constante **MFNETSOURCE \_ PROXYLOCATORFACTORY** define el GUID de esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden usar esta propiedad para proporcionar un localizador de proxy personalizado para el origen de red. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Compatibilidad con proxy para orígenes de red](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




