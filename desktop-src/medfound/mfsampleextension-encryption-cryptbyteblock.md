---
description: Especifica el tamaño del bloque de bytes cifrado para el cifrado de patrones basado en muestras.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: MFSampleExtension_Encryption_CryptByteBlock atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85da01a8b69fa22604cc10df54aa474ec117256ebee0630e490e25d9888484d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603205"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a>Atributo \_ CryptByteBlock de cifrado MFSampleExtension \_

Especifica el tamaño del bloque de bytes cifrado para el cifrado de patrones basado en muestras.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El número de bytes claros (no cifrados) en el bloque de asignación de submuestreo se especifica en el atributo [ \_ \_ SKIPByteBlock de cifrado MFSampleExtension.](mfsampleextension-encryption-skipbyteblock.md) Si alguno de estos atributos no está presente o tiene un valor de 0, significa que los datos de ejemplo no están cifrados. Ambos valores deben ser distintos de cero, valores positivos o ambos deben tener un valor de cero.

En los casos en los que el origen se basa en MP4, el valor se establece en función de los valores del bloque de bytes crypt predeterminado dentro del cuadro de cifrado de pista \_ \_ \_ ('tenc') en el encabezado MP4. Para obtener más información, [vea MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 




