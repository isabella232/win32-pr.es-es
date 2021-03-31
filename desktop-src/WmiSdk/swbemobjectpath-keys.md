---
description: La propiedad Keys del objeto SWbemObjectPath es un objeto SWbemNamedValueSet que contiene los enlaces de valor de clave. Esta propiedad es de solo lectura.
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath. Keys (Adoctint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082391"
---
# <a name="swbemobjectpathkeys-property"></a>SWbemObjectPath. Keys (propiedad)

La propiedad **Keys** del objeto [**SWbemObjectPath**](swbemobjectpath.md) es un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que contiene los enlaces de valor de clave. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Después de recuperar la propiedad **Keys** , el objeto **Err** puede contener el código de error siguiente.

<dl> <dt>

**wbemErrNotSupported** -2147749900 (0x8004100C)
</dt> <dd>

No se admite esta característica u operación. Se devuelve este error si un script intenta escribir en esta propiedad.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                             |
| Encabezado<br/>                   | <dl> <dt>Adoctint. h (incluye Wbemdisp. h)</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl>                    |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl>                    |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                                          |
| IID<br/>                      | \_ISWBEMOBJECTPATH IID<br/>                                                                           |



 

 




