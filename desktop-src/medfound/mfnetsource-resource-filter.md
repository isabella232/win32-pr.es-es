---
description: Contiene un puntero a la interfaz de devolución de llamada IMFNetResourceFilter para la secuencia de bytes HTTP Microsoft Media Foundation.
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: Propiedad MFNETSOURCE_RESOURCE_FILTER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811845"
---
# <a name="mfnetsource_resource_filter-property"></a>Propiedad de filtro de \_ recursos MFNETSOURCE \_

Contiene un puntero a la interfaz de devolución de llamada [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) para la secuencia de bytes http Microsoft Media Foundation.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**IUnknown \** _

VT \_ desconocido

_ *punkVal**



## <a name="remarks"></a>Observaciones

Utilice esta propiedad para configurar la secuencia de bytes HTTP Media Foundation. Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
