---
description: La propiedad Name de un objeto SWbemPrivilege es una cadena que describe de forma única un privilegio.
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: SWbemPrivilege.Name propiedad (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 45a64d0216fa202481d6213f74f7a3a0f06a1b6837d654e7b88b15035f21ba73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611675"
---
# <a name="swbemprivilegename-property"></a>SWbemPrivilege.Name propiedad

La **propiedad Name** de un objeto [**SWbemPrivilege**](swbemprivilege.md) es una cadena que describe de forma única un privilegio. Por ejemplo, el privilegio que controla si un usuario puede ejecutar el método de apagado de un objeto tiene la cadena "SeShutdownPrivilege" en la **SWbemPrivilege.Name** predeterminada. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilege<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemPrivilege<br/>                                                         |



 

 




