---
description: La tabla AppId o la tabla registry especifica que el instalador configure y registre servidores DCOM para realizar una de las siguientes acciones durante una instalación.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Tabla AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8452635cd7c167d6a8618629eaec2f6f6c1aa2e72e0b3628a7d4542a9e7160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066275"
---
# <a name="appid-table"></a>Tabla AppId

La tabla AppId o la [tabla registry](registry-table.md) especifica que el instalador configure y registre servidores DCOM para realizar una de las siguientes acciones durante una instalación.

-   Ejecute el servidor DCOM con una identidad diferente a la del usuario que activa el servidor. Por ejemplo, para configurar un servidor DCOM para que siempre se ejecute como un usuario interactivo o como un usuario predefinido.
-   Ejecute el servidor DCOM como servicio.
-   Configure el acceso de seguridad predeterminado para el servidor DCOM.
-   Registre el servidor DCOM de modo que se active en otro equipo.

Esta tabla se procesa durante la instalación del componente asociado al servidor DCOM en la \_ columna Componente de la tabla [Class](class-table.md). No se anuncia un AppId.

La tabla AppId tiene las columnas siguientes.



| Columna               | Tipo                       | Clave | Nullable |
|----------------------|----------------------------|-----|----------|
| AppId                | [GUID](guid.md)           | Y   | N        |
| RemoteServerName     | [Formato](formatted.md) | N   | Y        |
| LocalService (Servicio local)         | [Texto](text.md)           | N   | Y        |
| ServiceParameters    | [Texto](text.md)           | N   | Y        |
| DllSurrogate         | [Texto](text.md)           | N   | Y        |
| ActivateAtStorage    | [Entero](integer.md)     | N   | Y        |
| RunAsInteractiveUser | [Entero](integer.md)     | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="AppId"></span><span id="appid"></span><span id="APPID"></span>Appid
</dt> <dd>

La columna AppId de la [tabla Class es](class-table.md) una clave externa en esta columna de la tabla AppId. Esta columna contiene el valor de AppId que se escribirá en el CLSID y crea la clave GUID de AppId en HKCR \\ AppId.

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName
</dt> <dd>

Esta columna contiene el valor de "RemoteServerName"= <xxxx> que se escribirá en HKCR \\ AppID \\ {AppID}. \\

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService
</dt> <dd>

Esta columna contiene el valor de LocalService que se escribirá en HKCR \\ AppID \\ { } <appid> "LocalService"= <xxx> .

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters
</dt> <dd>

Esta columna contiene el valor de ServiceParameters que se escribirá en HKCR \\ AppID \\ {appid>} "ServiceParameters".

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate
</dt> <dd>

Esta columna contiene el valor de DllSurrogate que se escribirá en HKCR \\ AppId \\ { } <appid> "DllSurrogate"= <xxx> . Si esta columna está presente, normalmente será una cadena vacía.

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage
</dt> <dd>

Un valor entero distinto de cero en este campo hace que Windows Installer escriba HKCR \\ AppID \\ { } <appid> "ActivateAtStorage"="Y" en el Registro. Si el campo se deja vacío o tiene un valor de cero, no se escribirá ningún valor.

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser
</dt> <dd>

Un valor entero distinto de cero en este campo hace que Windows Installer escriba HKCR \\ AppID \\ {appid>} "RunAs"="Interactive User" en el Registro. Si el campo se deja vacío o tiene un valor de cero, no se escribirá ningún valor.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La acción [RegisterClassInfo](registerclassinfo-action.md) y la acción [UnregisterClassInfo](unregisterclassinfo-action.md)usan esta tabla.

Tenga en cuenta que la tabla AppId no tiene una columna para registrar un nombre predeterminado. Por lo tanto, en los casos en los que necesite escribir un nombre descriptivo como valor de nombre predeterminado, debe registrarse mediante la [tabla del Registro](registry-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



