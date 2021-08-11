---
description: Establece la asignación de sub sample para el ejemplo que indica los bytes claros y cifrados en los datos de ejemplo.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: MFSampleExtension_Encryption_SubSampleMappingSplit atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19f10f845b337ab92774f36b46940fe9d5203ca3a672f573e33fbcea26e96e16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240798"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a>Atributo MFSampleExtension \_ Encryption \_ SubSampleMappingSplit

Establece la asignación de sub sample para el ejemplo que indica los bytes claros y cifrados en los datos de ejemplo.

## <a name="data-type"></a>Tipo de datos

**Blob**

## <a name="remarks"></a>Comentarios

El **BLOB** debe contener una matriz de intervalos de bytes como DWORDs donde cada dos DWORDs crea un conjunto. El primer DWORD de cada conjunto es el número de bytes sin cifrar y el segundo DWORD del conjunto es el número de bytes cifrados. Tenga en cuenta que un par de 0s no es un conjunto válido (cualquier valor puede ser 0, pero no ambos). La matriz de intervalos de bytes indica qué intervalos descifrar, incluida la posibilidad de que no se descifre toda la muestra. Se recomienda que no se establezca en ejemplos claros, aunque es posible lograr el mismo resultado si se establece con los valores adecuados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer SUBSampleExtension \_ Encryption \_ SubSampleMappingSplit.


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MFSampleExtension \_ Content \_ KeyID](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




