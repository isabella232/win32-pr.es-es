---
description: Especifica el tamaño del bloque de bytes cifrado para el cifrado de patrones basado en muestras.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: MFSampleExtension_Encryption_CryptByteBlock atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574857"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a>Atributo \_ CryptByteBlock de cifrado MFSampleExtension \_

Especifica el tamaño del bloque de bytes cifrado para el cifrado de patrones basado en muestras.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El número de bytes claros (no cifrados) en el bloque de asignación de submuestreo se especifica en el atributo [ \_ \_ SKIPByteBlock de cifrado MFSampleExtension.](mfsampleextension-encryption-skipbyteblock.md) Si alguno de estos atributos no está presente o tiene un valor de 0, significa que los datos de ejemplo no están cifrados. Ambos valores deben ser distintos de cero, valores positivos o ambos deben tener un valor de cero.

En los casos en los que el origen está basado en MP4, el valor se establece en función de los valores del bloque de bytes crypt predeterminado dentro del cuadro de cifrado de pista \_ \_ \_ ('tenc') en el encabezado MP4. Para obtener más información, [vea MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 




