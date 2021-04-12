---
description: El método SWbemRefresher. Item devuelve el SWbemRefreshableItem especificado de la colección. SWbemRefreshableItem de la colección.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: Método SWbemRefresher. Item (Wbemdisp. h)
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
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279796"
---
# <a name="swbemrefresheritem-method"></a>SWbemRefresher. Item (método)

El método **SWbemRefresher. Item** devuelve el [**SWbemRefreshableItem**](swbemrefreshableitem.md) especificado de la colección.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lIndex* 
</dt> <dd>

Valor de índice del elemento de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la llamada se realiza correctamente, se devuelve el objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) especificado.

## <a name="error-codes"></a>Códigos de error

Si el actualizador no tiene ningún elemento con el índice especificado, se genera **wbemErrNotFound** .

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

 

 




