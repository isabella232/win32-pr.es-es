---
description: Contiene el subtipo de medio para un nodo de topología. Este atributo se establece cuando no se puede cargar la topología porque no se pudo encontrar el descodificador correcto.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: MF_TOPONODE_ERROR_SUBTYPE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715387"
---
# <a name="mf_toponode_error_subtype-attribute"></a>\_Atributo de \_ subtipo de error MF TOPONODE \_

Contiene el subtipo de medio para un nodo de topología. Este atributo se establece cuando no se puede cargar la topología porque no se pudo encontrar el descodificador correcto.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a todos los tipos de nodo.

El cargador de topología podría establecer el atributo. Las aplicaciones normalmente leen este atributo pero no lo establecen.

Para obtener una lista de los valores posibles, consulte [GUID de tipo de medio](media-type-guids.md).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




