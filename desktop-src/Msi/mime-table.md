---
description: La tabla MIME asocia un tipo de contenido MIME con una extensión de nombre de archivo o un CLSID para generar la información de extensión o servidor COM necesaria para la publicación del contenido MIME (Extensiones multipropósito de Correo electrónico de Internet).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Tabla MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261247"
---
# <a name="mime-table"></a>Tabla MIME

La tabla MIME asocia un tipo de contenido MIME con una extensión de nombre de archivo o un CLSID para generar la información de extensión o servidor COM necesaria para la publicación del contenido MIME (Extensiones multipropósito de Correo electrónico de Internet).

La tabla MIME tiene las columnas siguientes.



| Columna      | Tipo             | Clave | Nullable |
|-------------|------------------|-----|----------|
| ContentType | [Texto](text.md) | Y   | N        |
| Extensión\_ | [Texto](text.md) | N   | N        |
| CLSID       | [GUID](guid.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>Contenttype
</dt> <dd>

Esta columna es un identificador para el contenido MIME. Normalmente se escribe en forma de tipo o formato.

</dd> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extensión\_
</dt> <dd>

Esta columna contiene la extensión de servidor que se va a asociar al contenido MIME, sin el punto. Esta columna es una clave externa en la [tabla De extensión](extension-table.md). La tabla Extensión contiene información del servidor de extensiones de nombre de archivo que se usa como parte del anuncio.

</dd> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

Esta columna contiene el CLSID del servidor COM que se va a asociar al contenido MIME. El CLSID de esta columna puede ser una clave externa en la tabla [Class](class-table.md) o puede ser un CLSID que ya existe en el equipo del usuario. La tabla Clase contiene información relacionada con el servidor COM que se usa como parte del anuncio.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta [la acción RegisterMIMEInfo](registermimeinfo-action.md) o la acción [UnregisterMIMEInfo.](unregistermimeinfo-action.md) En el modo de anuncio, la acción RegisterMIMEInfo registra toda la información MIME de los servidores de la tabla MIME para la que está habilitada la característica correspondiente. De lo contrario, la acción registra información MIME para los servidores de la tabla MIME para la que la característica correspondiente está seleccionada actualmente para instalarse. La [acción UnregisterMIMEInfo anula](unregistermimeinfo-action.md) el registro de la información del Registro relacionada con MIME del sistema. La acción anula el registro de la información MIME de los servidores de la tabla MIME para la que la característica correspondiente está seleccionada actualmente para desinstalarse.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE32](ice32.md)  
</dl>

 

 



