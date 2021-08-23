---
description: Especifica el tamaño de bloque de bytes sin cifrar (no cifrado) para el cifrado de patrones basado en muestras.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: MFSampleExtension_Encryption_SkipByteBlock atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c674a7f7762f97a1978bd827795733d01b1dea3053898c5ecd30308373449b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603135"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a>Atributo \_ \_ SkipByteBlock de cifrado MFSampleExtension

Especifica el tamaño de bloque de bytes sin cifrar (no cifrado) para el cifrado de patrones basado en muestras.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El número de bytes cifrados en el bloque de asignación de submuestreo se especifica en el atributo [MFSampleExtension \_ Encryption \_ CryptByteBlock.](mfsampleextension-encryption-cryptbyteblock.md) Si alguno de estos atributos no está presente o tiene un valor de 0, significa que los datos de ejemplo no están cifrados. Ambos valores deben ser distintos de cero, valores positivos o ambos deben tener un valor de cero.

En los casos en los que el origen está basado en MP4, el valor se establece en función de los valores del bloque de bytes skip predeterminado dentro del cuadro de cifrado de pista \_ \_ \_ ('tenc') en el encabezado MP4. Para obtener más información, [vea MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 




