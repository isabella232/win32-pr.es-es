---
description: Especifica si el codificador debe comprobar la coherencia de los datos entre los pases al realizar la codificación VBR de dos pases. Lectura y escritura.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: MFPKEY_CHECKDATACONSISTENCY2P propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cef9c8c2a8e4fcd536ce73653e80e62282b40734cc695493d6cba4187c8f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954725"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>Propiedad MFPKEY \_ CHECKDATACONSISTENCY2P

Especifica si el codificador debe comprobar la coherencia de los datos entre los pases al realizar la codificación VBR de dos pases. Lectura y escritura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ TRUE**

## <a name="remarks"></a>Comentarios

Si deja esta propiedad en su valor predeterminado **de VARIANT \_ TRUE**, el codificador comprueba que los ejemplos de entrada coinciden entre los dos pases y produce un error si detecta una discrepancia. El escenario principal que conduce a una discrepancia es cuando la entrada procede de un dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista o Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
