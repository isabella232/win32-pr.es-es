---
description: Especifica la configuración predeterminada para el bit de copyright en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Propiedad AVEncMPACopyright (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd747de4f4351e5d540fcf8235194308457e0dcc985500f2743209061cedbdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824275"
---
# <a name="avencmpacopyright-property"></a>AvEncMPACopyright, propiedad

Especifica la configuración predeterminada para el bit de copyright en la secuencia de audio MPEG-1. Esta propiedad se aplica a los codificadores de audio MPEG.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncMPACopyright**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad puede tener los siguientes valores.



| Value          | Descripción           |
|----------------|-----------------------|
| VARIANT \_ FALSE | El bit de copyright está desactivado. |
| VARIANT \_ TRUE  | El bit de copyright está en.  |



 

## <a name="remarks"></a>Comentarios

El codificador puede invalidar esta configuración, en función del contenido de la secuencia de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




