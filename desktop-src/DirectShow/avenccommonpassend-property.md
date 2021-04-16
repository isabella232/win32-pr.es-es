---
description: Detiene el paso de codificación actual o consulta si la fase de codificación actual es la última.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Propiedad AVEncCommonPassEnd (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495640"
---
# <a name="avenccommonpassend-property"></a>Propiedad AVEncCommonPassEnd

Detiene el paso de codificación actual o consulta si la fase de codificación actual es la última.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonPassEnd**

## <a name="remarks"></a>Observaciones

Al establecer esta propiedad en **Variant \_ true** , finaliza la fase de codificación actual. Al establecer esta propiedad en **Variant \_ false** se termina la codificación Multipass.

Al leer esta propiedad, se consulta si la fase de codificación actual es la última.

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

 

 




