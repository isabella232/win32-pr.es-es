---
description: Establece la asignación de submuestra para el ejemplo que indica los bytes claros y cifrados de los datos de ejemplo.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: MFSampleExtension_Encryption_SubSampleMappingSplit atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720449"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a>MFSampleExtension \_ Encryption \_ SubSampleMappingSplit Attribute

Establece la asignación de submuestra para el ejemplo que indica los bytes claros y cifrados de los datos de ejemplo.

## <a name="data-type"></a>Tipo de datos

**BLOB**

## <a name="remarks"></a>Observaciones

El **BLOB** debe contener una matriz de intervalos de bytes como DWORD, donde cada dos DWORD crea un conjunto. El primer valor DWORD de cada conjunto es el número de bytes claros y el segundo valor DWORD del conjunto es el número de bytes cifrados. Tenga en cuenta que un par de 0s no es un conjunto válido (el valor puede ser 0, pero no ambos). La matriz de intervalos de bytes indica qué rangos se van a descifrar, incluida la posibilidad de que no se pueda descifrar toda la muestra. Se recomienda no establecerlo en ejemplos claros, aunque es posible lograr el mismo resultado si se establece con los valores adecuados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer el \_ cifrado MFSampleExtension \_ SubSampleMappingSplit.


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[ID. de contenido de MFSampleExtension \_ \_](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




