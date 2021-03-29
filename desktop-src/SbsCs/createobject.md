---
description: El método CreateObject del objeto Microsoft. Windows. ActCtx crea un objeto en el contexto del manifiesto actual.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: ActCtx. CreateObject (método)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277351"
---
# <a name="actctxcreateobject-method"></a>ActCtx. CreateObject (método)

El método **CreateObject** del objeto [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) crea un objeto en el contexto del manifiesto actual.

## <a name="syntax"></a>Sintaxis


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objectId* 
</dt> <dd>

Cadena que especifica el tipo de objeto que se va a crear. Por ejemplo, un ProgID de COM.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx se define como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetObject (Método)**](getobject.md)
</dt> </dl>

 

 




