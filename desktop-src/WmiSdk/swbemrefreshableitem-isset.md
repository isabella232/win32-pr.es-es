---
description: La propiedad SWbemRefreshableItem. IsSet es un valor booleano que indica si el objeto SWbemRefreshableItem representa un solo objeto o un conjunto de objetos. El objeto SWbemRefreshableItem representa un único objeto o un conjunto de objetos.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Propiedad SWbemRefreshableItem. IsSet (Wbemdisp. h)
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
ms.openlocfilehash: 71fb5f84ec7ad35f1d9beab32cb74db5b7591057
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697927"
---
# <a name="swbemrefreshableitemisset-property"></a>Propiedad SWbemRefreshableItem. IsSet

La propiedad **SWbemRefreshableItem. IsSet** es un valor booleano que indica si el objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) representa un solo objeto o un conjunto de objetos.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Si **SWbemRefreshableItem. IsSet** es **true**, el elemento representa un objeto [**SWbemObjectSet**](swbemobjectset.md) y la propiedad del [**objeto**](swbemrefreshableitem-object.md) será **null**. Si es **false**, el elemento representa un objeto [**SWbemObject**](swbemobject.md) y la propiedad del **objeto** es **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | \_ISWBEMREFRESHABLEITEM IID<br/>                                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefreshableItem**](swbemrefresher.md)
</dt> </dl>

 

 




