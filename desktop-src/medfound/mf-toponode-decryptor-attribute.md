---
description: Especifica si un objeto subyacente de nodos topología es un Decrypter.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: MF_TOPONODE_DECRYPTOR atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707171"
---
# <a name="mf_toponode_decryptor-attribute"></a>\_Atributo de \_ descifrador MF TOPONODE

Especifica si el objeto subyacente de un nodo topología es un Decrypter.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo se aplica a todos los tipos de nodo.

Si el valor de este atributo es distinto de cero, el objeto subyacente del nodo es un Decrypter.

Normalmente, las aplicaciones no usan este atributo directamente. La sesión multimedia establece este atributo cuando crea un nodo para un Decrypter, obtenido del método [**IMFInputTrustAuthority:: GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) .

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

 

 




