---
description: Especifica el modo de control de intervalo dinámico que usará el descodificador de audio.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: Propiedad MFPKEY_WMADEC_DRCMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275851"
---
# <a name="mfpkey_wmadec_drcmode-property"></a>\_ \_ Propiedad DRCMODE de MFPKEY WMADEC

Especifica el modo de control de intervalo dinámico que usará el descodificador de audio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACDRCSetting

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Este valor entero va de 0 a 2. Cuanto mayor sea el valor, menor será el intervalo dinámico de la salida de audio sin comprimir. Un valor de 0 indica que el códec no realiza ningún control de intervalo dinámico, es decir, el códec no modificará el intervalo dinámico inherente del contenido codificado.

Si este valor se establece en 1 o 2, el códec usará las siguientes propiedades para determinar el control de intervalo dinámico necesario:

-   [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md)
-   [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md)
-   [MFPKEY \_ WMADRC \_ AVGTARGET](mfpkey-wmadrc-avgtargetproperty.md)
-   [MFPKEY \_ WMADRC \_ PEAKTARGET](mfpkey-wmadrc-peaktargetproperty.md)

Si no proporciona valores de destino, el códec proporcionará el suyo propio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




