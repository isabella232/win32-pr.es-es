---
description: La tabla AppId o la tabla del registro especifica que el instalador configura y registra los servidores DCOM para realizar una de las siguientes acciones durante una instalación.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Tabla AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909109"
---
# <a name="appid-table"></a>Tabla AppId

La tabla AppId o la [tabla del registro](registry-table.md) especifica que el instalador configura y registra los servidores DCOM para realizar una de las siguientes acciones durante una instalación.

-   Ejecute el servidor DCOM con una identidad diferente a la del usuario que activa el servidor. Por ejemplo, para configurar un servidor DCOM para que se ejecute siempre como usuario interactivo o como usuario predefinido.
-   Ejecute el servidor DCOM como servicio.
-   Configure el acceso de seguridad predeterminado para el servidor DCOM.
-   Registre el servidor DCOM para que se active en otro equipo.

Esta tabla se procesa en la instalación del componente asociado al servidor DCOM en la \_ columna componente de la [tabla clase](class-table.md). No se anuncia un AppId.

La tabla AppId tiene las columnas siguientes.



| Columna               | Tipo                       | Clave | Nullable |
|----------------------|----------------------------|-----|----------|
| AppId                | [GUID](guid.md)           | Y   | N        |
| RemoteServerName     | [Formatea](formatted.md) | N   | Y        |
| LocalService (Servicio local)         | [Texto](text.md)           | N   | Y        |
| ServiceParameters    | [Texto](text.md)           | N   | Y        |
| DllSurrogate         | [Texto](text.md)           | N   | Y        |
| ActivateAtStorage    | [Entero](integer.md)     | N   | Y        |
| RunAsInteractiveUser | [Entero](integer.md)     | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId
</dt> <dd>

La columna AppId de la [tabla de clase](class-table.md) es una clave externa de esta columna de la tabla AppID. Esta columna contiene el valor AppId que se escribirá en el CLSID y creará la clave AppId GUID en HKCR \\ AppID.

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName
</dt> <dd>

Esta columna contiene el valor "RemoteServerName" = <xxxx> que se escribirá en HKCR \\ AppID \\ {AppID} \\ .

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService
</dt> <dd>

Esta columna contiene el valor de LocalService que se escribirá en HKCR \\ AppID \\ { <appid> } "LocalService" = <xxx> .

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters
</dt> <dd>

Esta columna contiene el valor de ServiceParameters que se escribirá en HKCR \\ AppID \\ {AppID>} "ServiceParameters".

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate
</dt> <dd>

Esta columna contiene el valor de DllSurrogate que se escribirá en HKCR \\ AppID \\ { <appid> } "DllSurrogate" = <xxx> . Si esta columna está presente, normalmente será una cadena vacía.

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage
</dt> <dd>

Un valor entero distinto de cero en este campo hace que Windows Installer escriba HKCR \\ AppID \\ { <appid> } "ActivateAtStorage" = "Y" en el registro. Si el campo se deja vacío o tiene un valor de cero, no se escribirá ningún valor.

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser
</dt> <dd>

Un valor entero distinto de cero en este campo hace que Windows Installer escriba el identificador \\ AppID \\ {AppID>} "runas" = "usuario interactivo" en el registro. Si el campo se deja vacío o tiene un valor de cero, no se escribirá ningún valor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta tabla la usan la [acción RegisterClassInfo](registerclassinfo-action.md) y la [acción UnregisterClassInfo](unregisterclassinfo-action.md).

Tenga en cuenta que la tabla AppId no tiene una columna para registrar un nombre predeterminado. Por lo tanto, en los casos en los que tenga que escribir un nombre descriptivo como el valor de nombre predeterminado, debe registrarse mediante la [tabla del registro](registry-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



