---
description: Recupera una matriz que contiene los identificadores de propiedad de paquete para el trazo especificado.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'IContextNode:: GetStrokePacketDescriptionById (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696537"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a>IContextNode:: GetStrokePacketDescriptionById (método)

Recupera una matriz que contiene los identificadores de propiedad de paquete para el trazo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lStrokeId* \[ de\]
</dt> <dd>

Identificador del trazo.

</dd> <dt>

*pulStrokePacketDescriptionCount* \[ in, out\]
</dt> <dd>

El número de propiedades de paquete en cada paquete.

</dd> <dt>

*ppStrokePacketDescriptionGuids* \[ enuncia\]
</dt> <dd>

Una matriz que contiene los identificadores de propiedad de paquete.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppStrokePacketDescriptionGuids* cuando ya no necesite la información.

 

\**ppStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquete incluidos para cada punto del trazo. Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetStrokePacketDataById**](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

