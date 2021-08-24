---
description: El método SetAsSingleton del objeto SWbemObjectPath fuerza a la ruta de acceso a una instancia wmi singleton de una clase. Una clase singleton es una clase que nunca puede tener más de una instancia.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Método SWbemObjectPath.SetAsSingleton (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4a8a46566990021a4de4fca95b2b524cc7ddc1f5a797d7e3bffd0dc34ee52186
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568265"
---
# <a name="swbemobjectpathsetassingleton-method"></a>Método SWbemObjectPath.SetAsSingleton

El **método SetAsSingleton** del objeto [**SWbemObjectPath**](swbemobjectpath.md) fuerza a la ruta de acceso a una instancia wmi singleton de una clase. Una clase singleton es una clase que nunca puede tener más de una instancia.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md). SWbemObjectPath

## <a name="syntax"></a>Sintaxis


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método SetAsSingleton,** el **objeto Err** puede contener el código de error siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

 




