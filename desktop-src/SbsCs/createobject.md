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
ms.openlocfilehash: 4161ccdcc2562405123d8cb5276aa1f849121c0271b6c6e3f23a32551f6f3dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142398"
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetObject (Método)**](getobject.md)
</dt> </dl>

 

 




