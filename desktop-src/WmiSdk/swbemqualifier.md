---
description: Puede usar las propiedades del objeto SWbemQualifier para representar un calificador único de un parámetro de clase, instancia, propiedad o método WMI. La llamada CreateObject de VBScript no puede crear este objeto.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Objeto SWbemQualifier (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070402"
---
# <a name="swbemqualifier-object"></a>Objeto SWbemQualifier

Puede usar las propiedades del objeto **SWbemQualifier** para representar un calificador único de un parámetro de clase, instancia, propiedad o método WMI. La llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript no puede crear este objeto.

## <a name="members"></a>Members

El **objeto SWbemQualifier** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto SWbemQualifier** tiene estas propiedades.



| Propiedad.                                                                       | Tipo de acceso           | Descripción                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [**IsAmended**](swbemqualifier-isamended.md)<br/>                       | Solo lectura<br/>  | Valor booleano que indica si este calificador se ha localizado mediante una operación de combinación.<br/> |
| [**IsLocal**](swbemqualifier-islocal.md)<br/>                           | Solo lectura<br/>  | Valor booleano que indica si este calificador es local.<br/>                                   |
| [**IsOveribleble**](swbemqualifier-isoverridable.md)<br/>               | Lectura y escritura<br/> | Valor booleano que indica si este calificador se puede invalidar cuando se propaga.<br/>          |
| [**Nombre**](swbemqualifier-name.md)<br/>                                 | Solo lectura<br/>  | Nombre de este calificador.<br/>                                                                    |
| [**PropagatesToInstance**](swbemqualifier-propagatestoinstance.md)<br/> | Lectura y escritura<br/> | Valor booleano que indica si este calificador se puede propagar a una instancia de .<br/>           |
| [**PropagatesToSubClass**](swbemqualifier-propagatestosubclass.md)<br/> | Solo lectura<br/>  | Valor booleano que indica si este calificador se puede propagar a una subclase.<br/>            |
| [**Valor**](swbemqualifier-value.md)<br/>                               | Lectura y escritura<br/> | Valor variant de este calificador. Esta es la propiedad predeterminada de este objeto .<br/>              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifier<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemQualifier<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




