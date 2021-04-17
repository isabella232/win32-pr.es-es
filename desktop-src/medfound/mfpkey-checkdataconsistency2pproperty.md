---
description: Especifica si el codificador debe comprobar la coherencia de los datos entre las pasadas al realizar la codificación VBR de dos pasos. Lectura y escritura.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: Propiedad MFPKEY_CHECKDATACONSISTENCY2P (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698626"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>\_Propiedad CHECKDATACONSISTENCY2P de MFPKEY

Especifica si el codificador debe comprobar la coherencia de los datos entre las pasadas al realizar la codificación VBR de dos pasos. Lectura y escritura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ bool**

## <a name="default-value"></a>Valor predeterminado

**VARIANTE \_ true**

## <a name="remarks"></a>Observaciones

Si deja esta propiedad en su valor predeterminado de **Variant \_ true**, el codificador comprueba que los ejemplos de entrada coinciden entre los dos pasos y produce un error si detecta una discrepancia. El escenario principal que conduce a una discrepancia es cuando la entrada procede de un dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista o Windows 7<br/>                                                   |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
