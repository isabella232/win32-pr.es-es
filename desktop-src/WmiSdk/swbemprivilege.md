---
description: El objeto SWbemPrivilege representa un único privilegio. La llamada CreateObject de VBScript no puede crear este objeto.
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: Objeto SWbemPrivilege (Wbemdisp.h)
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
ms.openlocfilehash: eeb9726f3aaf696d4e889ea32e39c85306271b7690f02b05d93fff80715f497b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097155"
---
# <a name="swbemprivilege-object"></a>Objeto SWbemPrivilege

El **objeto SWbemPrivilege** representa un único privilegio. La llamada **CreateObject** de VBScript no puede crear este objeto.

## <a name="members"></a>Miembros

El **objeto SWbemPrivilege** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto SWbemPrivilege** tiene estas propiedades.



| Propiedad                                                     | Tipo de acceso           | Descripción                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [**Displayname**](swbemprivilege-displayname.md)<br/> | Solo lectura<br/>  | Nombre para mostrar de este privilegio.<br/>                                       |
| [**Identificador**](swbemprivilege-identifier.md)<br/>   | Lectura/escritura<br/> | Entero que representa el privilegio que se va a establecer o recuperar.<br/> |
| [**IsEnabled**](swbemprivilege-isenabled.md)<br/>     | Lectura/escritura<br/> | Valor booleano que indica si este privilegio está habilitado.<br/>            |
| [**Nombre**](swbemprivilege-name.md)<br/>               | Solo lectura<br/>  | Nombre de este privilegio.<br/>                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilege<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemPrivilege<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejecución de operaciones con privilegios](executing-privileged-operations.md)
</dt> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




