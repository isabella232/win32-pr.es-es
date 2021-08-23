---
description: La propiedad CIMType del objeto SWbemProperty es un entero que se puede usar para determinar el tipo CIM de esta propiedad. Esta propiedad es de solo lectura.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Propiedad SWbemProperty.CIMType (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f3b92cca8d17af8814a7891d0d4f97c7e003b1a999a42c63b6abe59d50e8ac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991935"
---
# <a name="swbempropertycimtype-property"></a>Propiedad SWbemProperty.CIMType

La **propiedad CIMType** del [**objeto SWbemProperty**](swbemproperty.md) es un entero que se puede usar para determinar el tipo CIM de esta propiedad. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Para obtener más información sobre los tipos válidos para esta propiedad, vea [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).

Las instancias de objetos incrustados se almacenan en objetos compuestos como propiedades de tipo **CIM \_ OBJECT**. Para determinar la clase de un objeto incrustado en una instancia de una clase compuesta, debe examinar el calificador **CIMType** de la propiedad de tipo **CIM \_ OBJECT.**

Las referencias de objeto de una clase de asociación se almacenan en propiedades de tipo **CIM \_ REFERENCE**. Para determinar las rutas de acceso de objeto reales, debe examinar el **calificador CIMType** de la propiedad de tipo **CIM \_ REFERENCE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



 

 




