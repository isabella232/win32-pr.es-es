---
description: El objeto SWbemNamedValue representa un valor con nombre único que pertenece al objeto de colección SWbemNamedValueSet. La llamada CreateObject de VBScript no puede crear este objeto.
ms.assetid: 3f72afcd-6e10-4200-804d-918e3eb2862f
ms.tgt_platform: multiple
title: Objeto SWbemNamedValue (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue
- ISWbemNamedValue
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 50fb1439e3d844dc2b704f7e69ede298df44f60d32f72d40bcf01051811e227e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612175"
---
# <a name="swbemnamedvalue-object"></a>Objeto SWbemNamedValue

El **objeto SWbemNamedValue** representa un valor con nombre único que pertenece al objeto de colección [**SWbemNamedValueSet.**](swbemnamedvalueset.md) La llamada [**CreateObject**](creating-an-object-using-vbscript.md) de VBScript no puede crear este objeto.

## <a name="members"></a>Miembros

El **objeto SWbemNamedValue** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto SWbemNamedValue** tiene estas propiedades.



| Propiedad                                          | Tipo de acceso           | Descripción                                                                                    |
|:--------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Nombre**](swbemnamedvalue-name.md)<br/>   | Solo lectura<br/>  | Nombre del **elemento SWbemNamedValue.**<br/>                                               |
| [**Valor**](swbemnamedvalue-value.md)<br/> | Lectura/escritura<br/> | Valor del **elemento SWbemNamedValue.** Esta es la propiedad predeterminada de este objeto .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValue<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemNamedValue<br/>                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




