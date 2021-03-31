---
description: Especifica cómo el cargador de topología conecta este nodo de topología y si este nodo es opcional.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: MF_TOPONODE_CONNECT_METHOD atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278649"
---
# <a name="mf_toponode_connect_method-attribute"></a>\_Atributo de \_ método de conexión MF TOPONODE \_

Especifica cómo el cargador de topología conecta este nodo de topología y si este nodo es opcional.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a todos los tipos de nodo.

El valor del atributo es una **operación OR bit a bit** de las marcas de la enumeración del [**\_ \_ método de conexión MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) . Si no se establece este atributo, el valor predeterminado es **MF \_ Connect \_ permitir \_ descodificador**.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




