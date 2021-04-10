---
description: Lista de direcciones URL a las que el origen de red enviará información de registro.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: Propiedad MFNETSOURCE_LOGURL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154628"
---
# <a name="mfnetsource_logurl-property"></a>\_Propiedad LOGURL de MFNETSOURCE

Lista de direcciones URL a las que el origen de red enviará información de registro.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

Matriz de cadenas de caracteres anchos (**CALPWSTR**)

VT \_ Vector \| VT \_ LPWStr

**calpwstr**



## <a name="remarks"></a>Observaciones

La constante **MFNETSOURCE \_ LOGURL** define el GUID para esta clave de propiedad. El identificador de propiedad (PID) es cero.

Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red. Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

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
</dt> </dl>

 

 




