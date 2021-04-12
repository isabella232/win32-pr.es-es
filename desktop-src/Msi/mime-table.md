---
description: La tabla MIME asocia un tipo de contenido MIME con una extensión de nombre de archivo o un CLSID para generar la extensión o la información del servidor COM necesaria para el anuncio del contenido MIME (Extensiones multipropósito de correo Internet).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Tabla MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278152"
---
# <a name="mime-table"></a>Tabla MIME

La tabla MIME asocia un tipo de contenido MIME con una extensión de nombre de archivo o un CLSID para generar la extensión o la información del servidor COM necesaria para el anuncio del contenido MIME (Extensiones multipropósito de correo Internet).

La tabla MIME tiene las columnas siguientes.



| Columna      | Tipo             | Clave | Nullable |
|-------------|------------------|-----|----------|
| ContentType | [Texto](text.md) | Y   | N        |
| Extensión\_ | [Texto](text.md) | N   | N        |
| CLSID       | [GUID](guid.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType
</dt> <dd>

Esta columna es un identificador del contenido MIME. Normalmente se escribe en forma de tipo/formato.

</dd> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_
</dt> <dd>

Esta columna contiene la extensión de servidor que se va a asociar al contenido MIME, sin el punto. Esta columna es una clave externa de la [tabla de extensión](extension-table.md). La tabla de extensión contiene información del servidor de extensión de nombre de archivo que se usa como parte del anuncio.

</dd> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

Esta columna contiene el CLSID del servidor COM que se va a asociar al contenido MIME. El CLSID de esta columna puede ser una clave externa en la [tabla de clases](class-table.md) o puede ser un CLSID que ya existe en el equipo del usuario. La tabla de clases contiene información relacionada con el servidor COM que se utiliza como parte del anuncio.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta la acción [RegisterMIMEInfo](registermimeinfo-action.md) o la [acción UnregisterMIMEInfo](unregistermimeinfo-action.md) . En el modo de anuncio, la acción RegisterMIMEInfo registra toda la información MIME de los servidores de la tabla MIME para la que está habilitada la característica correspondiente. De lo contrario, la acción registra la información MIME para los servidores de la tabla MIME para la que está seleccionada actualmente la característica correspondiente. La [acción UnregisterMIMEInfo](unregistermimeinfo-action.md) anula el registro de la información del registro relacionada con MIME del sistema. La acción anula el registro de la información de MIME para los servidores de la tabla MIME para la que está seleccionada actualmente la característica correspondiente para desinstalarla.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE32](ice32.md)  
</dl>

 

 



