---
description: Especifica si el localizador de proxy debe utilizar un servidor proxy para las direcciones locales.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: Propiedad MFNETSOURCE_PROXYBYPASSFORLOCAL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808047"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a>\_Propiedad PROXYBYPASSFORLOCAL de MFNETSOURCE

Especifica si el localizador de proxy debe utilizar un servidor proxy para las direcciones locales.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Booleano (**Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden utilizar esta propiedad para configurar el localizador de proxy al crear el objeto de localizador de proxy. Para establecer la propiedad, pase un puntero **IPropertyStore** en el parámetro *pProxyConfig* de la función [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . El valor debe establecerse en 0 si el servidor proxy se va a usar para las direcciones locales; de lo contrario, un valor distinto de cero configura el localizador de proxy predeterminado para omitir el servidor proxy para las direcciones locales.

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

 

 




