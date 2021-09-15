---
description: Método CreateObject de Microsoft. Windows. El objeto ActCtx crea un objeto en el contexto del manifiesto actual.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: Método ActCtx.CreateObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271676"
---
# <a name="actctxcreateobject-method"></a>Método ActCtx.CreateObject

Método **CreateObject** de [**Microsoft.Windows. El objeto ActCtx**](microsoft-windows-actctx-object.md) crea un objeto en el contexto del manifiesto actual.

## <a name="syntax"></a>Sintaxis


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Idobjeto* 
</dt> <dd>

Cadena que especifica el tipo de objeto que se creará. Por ejemplo, un progID COM.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID IActCtx se define como \_ 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetObject (Método)**](getobject.md)
</dt> </dl>

 

 




