---
description: El método SWbemRefresher.Item devuelve el objeto SWbemRefreshableItem especificado de la colección. SWbemRefreshableItem de la colección.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: Método SWbemRefresher.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1290a395b9fc3f4e485a90822103ccb51b40edcc1b72fdf08433eaed72cdd213
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897575"
---
# <a name="swbemrefresheritem-method"></a>Método SWbemRefresher.Item

El **método SWbemRefresher.Item** devuelve el [**objeto SWbemRefreshableItem**](swbemrefreshableitem.md) especificado de la colección.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Lindex* 
</dt> <dd>

Valor de índice del elemento de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la llamada se realiza correctamente, se devuelve el objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) especificado.

## <a name="error-codes"></a>Códigos de error

Si el actualizador no tiene ningún elemento con el índice especificado, **se genera wbemErrNotFound.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




