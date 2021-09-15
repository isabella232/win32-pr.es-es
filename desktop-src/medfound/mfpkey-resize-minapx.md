---
description: Especifica la coordenada x de la esquina superior izquierda de la apertura de pantalla mínima.
ms.assetid: eb9e5330-fd89-4bca-ae8c-62985f9b2373
title: MFPKEY_RESIZE_MINAPX propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3325730bdd77d192abf79ed60e70a22363c398
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360692"
---
# <a name="mfpkey_resize_minapx-property"></a>Propiedad MFPKEY \_ RESIZE \_ DE MINAPX

Especifica la coordenada x de la esquina superior izquierda de la apertura de pantalla mínima.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="applies-to"></a>Se aplica a

-   [DSP de cambio de tamaño de vídeo](videoresizer.md)

## <a name="remarks"></a>Observaciones

El valor es un número real de punto fijo. La parte entera del número se almacena en los 2 bytes superiores y la parte fraccional se almacena en los 2 bytes inferiores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
