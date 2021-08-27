---
title: Objeto Session (WSManDisp.h)
description: Define las operaciones y la configuración de sesión.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Objeto de sesión Windows administración remota
- Objeto de sesión Windows administración remota , descrito
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b63ce9aa5898f3b6dad716f7af19688059ccf7a3f48901fa73ed3250cd2660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121565"
---
# <a name="session-object-wsmandisph"></a>Objeto Session (WSManDisp.h)

Define las operaciones y la configuración de sesión. Cualquier Windows de administración remota requiere la creación de una sesión que se conecte **a** un equipo remoto, al controlador de administración [*base*](windows-remote-management-glossary.md) (BMC) o al equipo local. Las operaciones de red de WinRM incluyen obtener, escribir o enumerar datos o invocar métodos. Los métodos del **objeto Session** reflejan las operaciones básicas definidas en WS-Management protocolo.

## <a name="members"></a>Miembros

El **objeto Session** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Session** tiene estos métodos.



| Método                                 | Descripción                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Crear**](session-create.md)       | Crea una nueva instancia de un recurso y devuelve el URI del nuevo objeto.<br/>                                      |
| [**Eliminar**](session-delete.md)       | Elimina el recurso especificado en el URI del recurso.<br/>                                                              |
| [**Enumerar**](session-enumerate.md) | Enumera un recurso de colección, tabla o registro de mensajes.<br/>                                                         |
| [**Obtener**](session-get.md)             | Recupera un recurso del servicio y devuelve una representación XML de la instancia actual del recurso.<br/> |
| [**Identificar**](session-identify.md)   | Consulta un equipo remoto para determinar si admite el protocolo WS-Management datos<br/>                                 |
| [**Invocar**](session-invoke.md)       | Invoca un método que devuelve los resultados de la llamada al método.<br/>                                                    |
| [**Poner**](session-put.md)             | Actualiza un recurso.<br/>                                                                                              |



 

### <a name="properties"></a>Propiedades

El **objeto Session** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso           | Descripción                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchItems**](session-batchitems.md)<br/> | Lectura/escritura<br/> | Establece y obtiene el número de elementos de cada lote de enumeración. Este valor no se puede cambiar durante una enumeración. De forma predeterminada, el valor predeterminado es un número ilimitado de elementos. El proveedor de recursos puede establecer un límite.<br/> |
| [**Error**](session-error.md)<br/>           | Solo lectura<br/>  | Obtiene información de error adicional en una secuencia XML.<br/>                                                                                                                                                              |
| [**Timeout**](session-timeout.md)<br/>       | Lectura/escritura<br/> | Establece y obtiene la cantidad máxima de tiempo (en milisegundos) que debe esperar la aplicación cliente.<br/>                                                                                                                   |



 

## <a name="remarks"></a>Comentarios

El **objeto Session** corresponde a la interfaz [**IWSManSession.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se muestra cómo crear un **objeto Session.**


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[WinRM Scripting API](winrm-scripting-api.md)
</dt> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dt>

[Scripting en Windows administración remota](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtener datos del equipo local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtener datos de un equipo remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





