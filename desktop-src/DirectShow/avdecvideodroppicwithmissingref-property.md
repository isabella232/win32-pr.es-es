---
description: Especifica si el descodificador quita las tramas dentro de las que faltan fotogramas de referencia.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Propiedad AVDecVideoDropPicWithMissingRef (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274690"
---
# <a name="avdecvideodroppicwithmissingref-property"></a>Propiedad AVDecVideoDropPicWithMissingRef

Especifica si el descodificador quita las tramas dentro de las que faltan fotogramas de referencia.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoDropPicWithMissingRef**

## <a name="remarks"></a>Observaciones

Si el fragmentada está dañado, es posible que falten fotogramas de referencia en un fotograma. Si el valor de esta propiedad es **Variant \_ true**, el descodificador quita el marco. Si el valor es **Variant \_ false**, el descodificador intenta descodificar el fotograma, utilizando uno o más fotogramas cercanos como fotogramas de referencia. El marco descodificado resultante tendrá artefactos de bloqueo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




