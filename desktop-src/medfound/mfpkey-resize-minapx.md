---
description: Especifica la coordenada x de la esquina superior izquierda de la apertura de pantalla mínima.
ms.assetid: eb9e5330-fd89-4bca-ae8c-62985f9b2373
title: MFPKEY_RESIZE_MINAPX propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb57c2ec8828c9efff0d321d68c5099a1809e49ae26539a131e287a40e4f2644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953555"
---
# <a name="mfpkey_resize_minapx-property"></a>Propiedad MFPKEY \_ RESIZE \_ DE MINAPX

Especifica la coordenada x de la esquina superior izquierda de la apertura de pantalla mínima.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="applies-to"></a>Se aplica a

-   [DSP de cambio de tamaño de vídeo](videoresizer.md)

## <a name="remarks"></a>Comentarios

El valor es un número real de punto fijo. La parte entera del número se almacena en los 2 bytes superiores y la parte fraccional se almacena en los 2 bytes inferiores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
