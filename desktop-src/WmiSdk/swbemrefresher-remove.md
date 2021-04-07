---
description: El método SWbemRefresher. Remove quita el objeto SWbemRefreshableItem con el índice especificado del actualizador.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Método SWbemRefresher. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003394"
---
# <a name="swbemrefresherremove-method"></a>SWbemRefresher. Remove (método)

El método **SWbemRefresher. Remove** quita el objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) con el índice especificado del actualizador. El objeto **SWbemRefreshableItem** puede representar un solo objeto o un conjunto de objetos.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LIndex* 
</dt> <dd>

Índice del elemento en el objeto [**SWbemRefresher**](swbemrefresher.md) .

</dd> <dt>

*iFlags* \[ opta\]
</dt> <dd>

Las marcas deben establecer T0 (cero).

</dd> <dt>

*objWbemNamedvalueSet* \[ opta\]
</dt> <dd>

NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

**Códigos de error** Si el actualizador no tiene ningún elemento con el índice especificado, se genera **wbemErrNotFound** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | \_ISWBEMREFRESHER IID<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




