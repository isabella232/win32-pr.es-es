---
description: El objeto SWbemPrivilege representa un solo privilegio. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: Objeto SWbemPrivilege (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege
- ISWbemPrivilege
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c3be448b4088011cd4d628a7d98b448af550b010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083382"
---
# <a name="swbemprivilege-object"></a>Objeto SWbemPrivilege

El objeto **SWbemPrivilege** representa un solo privilegio. Este objeto no se puede crear mediante la llamada **CreateObject** de VBScript.

## <a name="members"></a>Miembros

El objeto **SWbemPrivilege** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **SWbemPrivilege** tiene estas propiedades.



| Propiedad                                                     | Tipo de acceso           | Descripción                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [**Mostrar**](swbemprivilege-displayname.md)<br/> | Solo lectura<br/>  | Nombre para mostrar de este privilegio.<br/>                                       |
| [**Identificador**](swbemprivilege-identifier.md)<br/>   | Lectura/escritura<br/> | Entero que representa el privilegio que se va a establecer o recuperar.<br/> |
| [**IsEnabled**](swbemprivilege-isenabled.md)<br/>     | Lectura/escritura<br/> | Valor booleano que indica si este privilegio está habilitado.<br/>            |
| [**Name**](swbemprivilege-name.md)<br/>               | Solo lectura<br/>  | Nombre de este privilegio.<br/>                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilege<br/>                                                        |
| IID<br/>                      | \_ISWBEMPRIVILEGE IID<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejecutar operaciones con privilegios](executing-privileged-operations.md)
</dt> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

 




