---
description: La propiedad CIMType del objeto SWbemProperty es un entero que se puede utilizar para determinar el tipo CIM de esta propiedad. Esta propiedad es de solo lectura.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Propiedad SWbemProperty. CIMType (Wbemdisp. h)
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
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002118"
---
# <a name="swbempropertycimtype-property"></a>Propiedad SWbemProperty. CIMType

La propiedad **CIMType** del objeto [**SWbemProperty**](swbemproperty.md) es un entero que se puede utilizar para determinar el tipo CIM de esta propiedad. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Para obtener más información sobre los tipos válidos para esta propiedad, vea [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).

Las instancias de objetos incrustados se almacenan en objetos compuestos como propiedades del tipo de **\_ objeto CIM**. Para determinar la clase de un objeto incrustado en una instancia de una clase compuesta, debe examinar el calificador **CIMType** de la propiedad tipo de **\_ objeto CIM** .

Las referencias de objeto en una clase de asociación se almacenan en las propiedades de tipo **\_ referencia CIM**. Para determinar las rutas de acceso de objeto reales, debe examinar el calificador **CIMType** de la propiedad tipo de **\_ referencia CIM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | \_ISWBEMPROPERTY IID<br/>                                                          |



 

 




