---
description: Especifica si se deben cargar transformaciones de Microsoft Media Foundation hardware (MTA) en la topología.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: MF_TOPOLOGY_HARDWARE_MODE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52da08dc1da36072f02627ec632bb8caf189c1748545c1ded5c3e4ebdedc1234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875672"
---
# <a name="mf_topology_hardware_mode-attribute"></a>Atributo \_ MF TOPOLOGY \_ HARDWARE \_ MODE

Especifica si se deben cargar transformaciones de Microsoft Media Foundation hardware (MTA) en la topología.

## <a name="data-type"></a>Tipo de datos

**[**MFTOPOLOGY \_ MODO HARDWARE \_ almacenado**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentarios

Este atributo es opcional. Establezca el atributo antes de resolver la topología.



| Valor                                  | Descripción                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFTOPOLOGY \_ HWMODE \_ USE \_ HARDWARE**  | El cargador de topologías cargará los MFT basados en hardware, como los descodificadores de hardware, cuando estén disponibles.<br/> El cargador de topologías vuelve automáticamente a la descodificación de software si no se encuentra ningún descodificador de hardware o si un descodificador de hardware no se puede conectar por algún motivo.<br/> |
| **MFTOPOLOGY \_ HWMODE \_ SOFTWARE \_ ONLY** | El cargador de topologías solo cargará los MTA de software, incluidos los descodificadores de software.                                                                                                                                                                                                    |



 

El valor predeterminado es **MFTOPOLOGY \_ HWMODE \_ SOFTWARE \_ ONLY**, por compatibilidad con las aplicaciones existentes. El valor recomendado es **MFTOPOLOGY \_ HWMODE \_ USE \_ HARDWARE**.

Si el cargador de topologías inserta un MFT de hardware en la topología, establece el atributo [MFT \_ ENUM \_ HARDWARE URL \_ \_ Attribute](mft-enum-hardware-url-attribute.md) en el nodo de topología. Para comprobar si hay un MFT de hardware, enumere los nodos de la topología resuelta y compruebe si este atributo está presente.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




