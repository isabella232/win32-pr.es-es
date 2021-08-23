---
description: Establece o recupera el nombre del proveedor de servicios criptográficos (CSP).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: Propiedad ISCrdEnr::CSPName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 7a1b5b443807dfe7fa737cdfc5eb4da678845e53b555ffe6eebf1529583fdb35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005233"
---
# <a name="iscrdenrcspname-property"></a>Propiedad ISCrdEnr::CSPName

La **propiedad CSPName** establece o recupera el nombre del proveedor [*de servicios criptográficos*](../secgloss/c-gly.md) (CSP).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre del CSP.

## <a name="error-codes"></a>Códigos de error

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

## <a name="remarks"></a>Comentarios

Establezca esta propiedad para especificar el nombre del CSP que se va a usar con el control de inscripción de tarjeta inteligente. Obtenga esta propiedad para recuperar el nombre del CSP especificado. Si no especifica un valor para esta propiedad, la propiedad **CSPName** tiene como valor predeterminado el nombre de la lista disponible de CSP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr se define como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::CSPCount**](iscrdenr-cspcount.md)
</dt> <dt>

[**ISCrdEnr::enumCSPName**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
