---
description: Especifica el tamaño del bloque de bytes cifrado para el cifrado del modelo basado en el ejemplo.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: MFSampleExtension_Encryption_CryptByteBlock atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082436"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a>MFSampleExtension \_ Encryption \_ CryptByteBlock Attribute

Especifica el tamaño del bloque de bytes cifrado para el cifrado del modelo basado en el ejemplo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El número de bytes claros (no cifrados) en el bloque de asignación de submuestra se especifica en el atributo [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) . Si alguno de estos atributos no está presente o tiene un valor de 0, significa que los datos de ejemplo no están cifrados. Ninguno de estos valores debe ser distinto de cero, los valores positivos o ambos deben tener un valor de cero.

En los casos en los que el origen está basado en MP4, el valor se establece en función de los valores del \_ bloque de bytes de cifrado predeterminado en \_ \_ el cuadro seguimiento de cifrado (' tenc ') en el encabezado MP4. Para obtener más información, vea [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 




