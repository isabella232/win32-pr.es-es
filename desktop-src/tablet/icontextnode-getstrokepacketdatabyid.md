---
description: Recupera una matriz que contiene los datos de propiedad del paquete para el trazo especificado.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: Método IContextNode::GetStrokePacketDataById (IACom.h)
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
ms.openlocfilehash: f80ad2e4acc88f24a14e21f604eb17dbab51a5bdeca0fc90ffc3ca9beb99f1de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967384"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a>IContextNode::GetStrokePacketDataById (método)

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

*strokeId* \[ En\]
</dt> <dd>

Identificador del trazo.

</dd> <dt>

*pStrokePacketDataCount* \[ in, out\]
</dt> <dd>

Longitud de la matriz de datos de paquetes.

</dd> <dt>

*pplStrokePacketData* \[ out\]
</dt> <dd>

Puntero a los datos del paquete para el trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *pplStrokePacketData* cuando ya no necesite la información.

 

*plStrokePacketData contiene* datos de paquetes para todos los puntos del trazo. Para obtener los tipos de datos de paquete incluidos para cada punto del trazo, use [**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

