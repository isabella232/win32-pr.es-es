---
description: Recupera una matriz que contiene los datos de propiedad del paquete para el trazo especificado.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'IContextNode:: GetStrokePacketDataById (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696538"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a>IContextNode:: GetStrokePacketDataById (método)

Recupera una matriz que contiene los datos de propiedad del paquete para el trazo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strokeId* \[ de\]
</dt> <dd>

Identificador del trazo.

</dd> <dt>

*pStrokePacketDataCount* \[ in, out\]
</dt> <dd>

La longitud de la matriz de datos de paquetes.

</dd> <dt>

*pplStrokePacketData* \[ enuncia\]
</dt> <dd>

Puntero a los datos del paquete del trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *pplStrokePacketData* cuando ya no necesite la información.

 

*plStrokePacketData* contiene datos de paquetes para todos los puntos del trazo. Para obtener los tipos de datos de paquete incluidos para cada punto del trazo, use [**IContextNode:: GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).

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

[**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

