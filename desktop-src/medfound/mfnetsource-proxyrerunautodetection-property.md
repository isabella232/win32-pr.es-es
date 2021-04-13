---
description: Especifica si el localizador de proxy predeterminado debe forzar la detección automática del proxy.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: Propiedad MFNETSOURCE_PROXYRERUNAUTODETECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37021c7e96b135389f0dffa2f8c26b8067df2b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544326"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a>\_Propiedad PROXYRERUNAUTODETECTION de MFNETSOURCE

Especifica si el localizador de proxy predeterminado debe forzar la detección automática del proxy.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Booleano (**Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PROXYSETTINGS** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden utilizar esta propiedad para configurar el localizador de proxy al crear el objeto de localizador de proxy. Para establecer la propiedad, pase un puntero **IPropertyStore** en el parámetro *pProxyConfig* de la función [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . En el modo de detección automática, el localizador proxy utiliza el mecanismo de detección de proxy WinInet. Para forzar la detección automática, establezca el valor en 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Funciones de red en Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Compatibilidad con proxy para orígenes de red](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




