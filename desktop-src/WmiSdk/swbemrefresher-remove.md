---
description: El método SWbemRefresher.Remove quita el objeto SWbemRefreshableItem con el índice especificado del actualizador.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Método SWbemRefresher.Remove (Wbemdisp.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465493"
---
# <a name="swbemrefresherremove-method"></a>Método SWbemRefresher.Remove

El **método SWbemRefresher.Remove** quita el objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) con el índice especificado del actualizador. El **objeto SWbemRefreshableItem** puede representar un único objeto o un conjunto de objetos.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

*Lindex* 
</dt> <dd>

Índice del elemento en el [**objeto SWbemRefresher.**](swbemrefresher.md)

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Las marcas deben establecerse en t0 (cero).

</dd> <dt>

*objWbemNamedvalueSet* \[ Opcional\]
</dt> <dd>

NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no tiene valores devueltos.

## <a name="remarks"></a>Observaciones

**Códigos de error** Si el actualizador no tiene ningún elemento con el índice especificado, **se genera wbemErrNotFound.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




