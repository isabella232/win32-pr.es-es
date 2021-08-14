---
description: La propiedad SWbemRefreshableItem.IsSet es un valor booleano que indica si el objeto SWbemRefreshableItem representa un único objeto o un conjunto de objetos. El objeto SWbemRefreshableItem representa un único objeto o un conjunto de objetos.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Propiedad SWbemRefreshableItem.IsSet (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055c776c1beffe1550033d61b54256d7b2e983ca70ac13f1b9fc899920910d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312924"
---
# <a name="swbemrefreshableitemisset-property"></a>Propiedad SWbemRefreshableItem.IsSet

La **propiedad SWbemRefreshableItem.IsSet** es un valor booleano que indica si el objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) representa un único objeto o un conjunto de objetos.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Si **SWbemRefreshableItem.IsSet** es **TRUE**, el elemento representa un objeto [**SWbemObjectSet**](swbemobjectset.md) y la propiedad [**Object**](swbemrefreshableitem-object.md) será **NULL.** Si **es FALSE,** el elemento representa un [**objeto SWbemObject**](swbemobject.md) y la **propiedad Object** es **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | IID \_ ISWbemRefreshableItem<br/>                                                   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefreshableItem**](swbemrefresher.md)
</dt> </dl>

 

 




