---
description: El método GetObject obtiene una instancia de un microsoft existente. Windows. Objeto ActCtx.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: Método ActCtx.GetObject
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
ms.openlocfilehash: b6c47c00f50cdeaa97fd0fafcd8aefa3c4863bc1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271572"
---
# <a name="actctxgetobject-method"></a>Método ActCtx.GetObject

El **método GetObject** obtiene una instancia de un archivo [**Microsoft.Windows. Objeto ActCtx.**](microsoft-windows-actctx-object.md)

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

Cadena obligatoria que indica el objeto . El nombre debe estar en el Registro en **HKEY \_ LOCAL \_ MACHINE** \\ **Microsoft** \\ **Visual Studio** \\ **6.0** \\ **&lt; &gt; package** \\ **Automation**.

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

[**CreateObject (método)**](createobject.md)
</dt> </dl>

 

 




