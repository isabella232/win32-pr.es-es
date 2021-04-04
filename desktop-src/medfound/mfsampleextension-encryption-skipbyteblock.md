---
description: Especifica el tamaño de bloque de bytes sin cifrar (sin cifrar) para el cifrado del modelo basado en el ejemplo.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: MFSampleExtension_Encryption_SkipByteBlock atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18003c03df7e65314846d34cb1d1093f5b2507a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908651"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a>MFSampleExtension \_ Encryption \_ SkipByteBlock Attribute

Especifica el tamaño de bloque de bytes sin cifrar (sin cifrar) para el cifrado del modelo basado en el ejemplo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El número de bytes cifrados en el bloque de asignación de submuestra se especifica en el atributo [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) . Si alguno de estos atributos no está presente o tiene un valor de 0, significa que los datos de ejemplo no están cifrados. Ninguno de estos valores debe ser distinto de cero, los valores positivos o ambos deben tener un valor de cero.

En los casos en los que el origen está basado en MP4, el valor se establece en función de los valores de \_ omitir el \_ bloque de bytes predeterminado \_ en el cuadro de cifrado de seguimiento (' tenc ') en el encabezado MP4. Para obtener más información, vea [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 




