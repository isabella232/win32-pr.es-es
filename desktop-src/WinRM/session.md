---
title: Objeto de sesión (WSManDisp. h)
description: Define las operaciones y la configuración de la sesión.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de objeto de sesión
- Administración remota de Windows de objeto de sesión, descrito
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
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997144"
---
# <a name="session-object-wsmandisph"></a>Objeto de sesión (WSManDisp. h)

Define las operaciones y la configuración de la sesión. Cualquier operación de Administración remota de Windows requiere la creación de una **sesión** que se conecta a un equipo remoto, un [*controlador de administración de base*](windows-remote-management-glossary.md) (BMC) o el equipo local. Las operaciones de red de WinRM incluyen la obtención, escritura o enumeración de datos, o la invocación de métodos. Los métodos del objeto de **sesión** reflejan las operaciones básicas definidas en el protocolo WS-Management.

## <a name="members"></a>Miembros

El objeto de **sesión** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **sesión** tiene estos métodos.



| Método                                 | Descripción                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**A**](session-create.md)       | Crea una nueva instancia de un recurso y devuelve el URI del nuevo objeto.<br/>                                      |
| [**Elimínelos**](session-delete.md)       | Elimina el recurso especificado en el URI del recurso.<br/>                                                              |
| [**Enumerar**](session-enumerate.md) | Enumera una colección, una tabla o un recurso de registro de mensajes.<br/>                                                         |
| [**Obtener**](session-get.md)             | Recupera un recurso del servicio y devuelve una representación XML de la instancia actual del recurso.<br/> |
| [**Identificar**](session-identify.md)   | Consulta un equipo remoto para determinar si es compatible con el protocolo de WS-Management<br/>                                 |
| [**Invocar**](session-invoke.md)       | Invoca un método que devuelve los resultados de la llamada al método.<br/>                                                    |
| [**Pondrán**](session-put.md)             | Actualiza un recurso.<br/>                                                                                              |



 

### <a name="properties"></a>Propiedades

El objeto de **sesión** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso           | Descripción                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchItems**](session-batchitems.md)<br/> | Lectura/escritura<br/> | Establece y obtiene el número de elementos de cada lote de enumeración. Este valor no se puede cambiar durante una enumeración. De forma predeterminada, el valor predeterminado es un número ilimitado de elementos. El proveedor de recursos puede establecer un límite.<br/> |
| [**Error**](session-error.md)<br/>           | Solo lectura<br/>  | Obtiene información de error adicional en una secuencia XML.<br/>                                                                                                                                                              |
| [**Tiempo de espera**](session-timeout.md)<br/>       | Lectura/escritura<br/> | Establece y obtiene el tiempo máximo (en milisegundos) que la aplicación cliente debe esperar.<br/>                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

El objeto de **sesión** corresponde a la interfaz [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) .

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se muestra cómo crear un objeto de **sesión** .


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
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de scripting de WinRM](winrm-scripting-api.md)
</dt> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[Scripting en Administración remota de Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtención de datos del equipo local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtención de datos de un equipo remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





