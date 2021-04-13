---
description: Puede utilizar las propiedades del objeto SWbemQualifier para representar un único calificador de una clase WMI, una instancia, una propiedad o un parámetro de método. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Objeto SWbemQualifier (Wbemdisp. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276118"
---
# <a name="swbemqualifier-object"></a>Objeto SWbemQualifier

Puede utilizar las propiedades del objeto **SWbemQualifier** para representar un único calificador de una clase WMI, una instancia, una propiedad o un parámetro de método. Este objeto no se puede crear mediante la llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript.

## <a name="members"></a>Miembros

El objeto **SWbemQualifier** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **SWbemQualifier** tiene estas propiedades.



| Propiedad                                                                       | Tipo de acceso           | Descripción                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [**IsAmended**](swbemqualifier-isamended.md)<br/>                       | Solo lectura<br/>  | Valor booleano que indica si se ha traducido este calificador mediante una operación de combinación.<br/> |
| [**IsLocal**](swbemqualifier-islocal.md)<br/>                           | Solo lectura<br/>  | Valor booleano que indica si este calificador es local.<br/>                                   |
| [**IsOverridable**](swbemqualifier-isoverridable.md)<br/>               | Lectura/escritura<br/> | Valor booleano que indica si se puede invalidar este calificador al propagarse.<br/>          |
| [**Name**](swbemqualifier-name.md)<br/>                                 | Solo lectura<br/>  | Nombre de este calificador.<br/>                                                                    |
| [**PropagatesToInstance**](swbemqualifier-propagatestoinstance.md)<br/> | Lectura/escritura<br/> | Valor booleano que indica si se puede propagar este calificador a una instancia de.<br/>           |
| [**PropagatesToSubClass**](swbemqualifier-propagatestosubclass.md)<br/> | Solo lectura<br/>  | Valor booleano que indica si este calificador se puede propagar a una subclase.<br/>            |
| [**Value**](swbemqualifier-value.md)<br/>                               | Lectura/escritura<br/> | Valor de variante de este calificador. Esta es la propiedad predeterminada de este objeto.<br/>              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifier<br/>                                                        |
| IID<br/>                      | \_ISWBEMQUALIFIER IID<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

 




