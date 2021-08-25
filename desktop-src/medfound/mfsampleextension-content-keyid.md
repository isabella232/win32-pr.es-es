---
description: Establece el identificador de clave del ejemplo.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: MFSampleExtension_Content_KeyID atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38498665dddaed0cd38082246f61f0f86c9b1b7a1e8cec7d19d476c860fe8d6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848175"
---
# <a name="mfsampleextension_content_keyid-attribute"></a>Atributo KEYID de contenido MFSampleExtension \_ \_

Establece el identificador de clave del ejemplo.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer el identificador de clave para el ejemplo.


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**SAMPLESample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[SubSampleExtension \_ Encryption \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




