---
description: El método GetObject obtiene una instancia de un objeto Microsoft. Windows. ActCtx existente.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx. GetObject (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809373"
---
# <a name="actctxgetobject-method"></a>ActCtx. GetObject (método)

El método **GetObject** obtiene una instancia de un objeto [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) existente.

## <a name="syntax"></a>Sintaxis


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrName* 
</dt> <dd>

Cadena requerida que indica el objeto. El nombre debe estar en el registro en **HKEY \_ local \_ Machine** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.

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

[**CreateObject (método)**](createobject.md)
</dt> </dl>

 

 




