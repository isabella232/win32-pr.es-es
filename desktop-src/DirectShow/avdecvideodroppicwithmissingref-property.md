---
description: Especifica si el descodificador coloca fotogramas dentro de los que faltan fotogramas de referencia.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Propiedad AVDecVideoDropPicWithMissingRef (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162105"
---
# <a name="avdecvideodroppicwithmissingref-property"></a>AvDecVideoDropPicWithMissingRef, propiedad

Especifica si el descodificador coloca fotogramas dentro de los que faltan fotogramas de referencia.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoDropPicWithMissingRef**

## <a name="remarks"></a>Observaciones

Si la secuencia de bits está dañada, es posible que falte un marco de referencia. Si el valor de esta propiedad es **VARIANT \_ TRUE,** el descodificador quita el marco. Si el valor es **VARIANT \_ FALSE,** el descodificador intenta descodificar el fotograma, usando uno o varios fotogramas cercanos como fotogramas de referencia. El marco descodificado resultante tendrá artefactos de bloqueo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




