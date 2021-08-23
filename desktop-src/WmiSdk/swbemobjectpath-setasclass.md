---
description: El método SetAsClass del objeto SWbemObjectPath fuerza la ruta de acceso a una clase WMI.
ms.assetid: d341b980-bac9-4db4-a55f-eb971fb385da
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath.SetAsClass (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsClass
- ISWbemObjectPath.SetAsClass
- ISWbemObjectPath.put_SetAsClass
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2083dd2ef3d6edd40148a11b6a3d034d4199b2507855b53c164de3c34ba0a93f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503735"
---
# <a name="swbemobjectpathsetasclass-property"></a>Propiedad SWbemObjectPath.SetAsClass

El **método SetAsClass** del objeto [**SWbemObjectPath**](swbemobjectpath.md) fuerza la ruta de acceso a una clase WMI.

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.SetAsClass
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Después de obtener o establecer la **propiedad SetAsClass,** el **objeto Err** puede contener el código de error siguiente.

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



 

 




