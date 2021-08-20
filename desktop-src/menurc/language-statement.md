---
title: Language (Instrucción)
description: Define el idioma de todos los recursos hasta la siguiente instrucción LANGUAGE o hasta el final del archivo.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Menús de instrucciones LANGUAGE y otros recursos
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40971044f12897cd9c797fc2a2c44b0f34f81f4e1323e9689ea70905cac76da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687470"
---
# <a name="language-statement"></a>Language (Instrucción)

Define el idioma de todos los recursos hasta la siguiente **instrucción LANGUAGE** o hasta el final del archivo.

Cuando la **instrucción LANGUAGE** aparece antes del principio del cuerpo de una definición de recursos [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX,**](dialogex-resource.md) [**MENU,**](menu-resource.md) [**RCDATA**](rcdata-resource.md)o [**STRINGTABLE,**](stringtable-resource.md) el idioma especificado solo se aplica a ese recurso.

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span id="language"></span><span id="LANGUAGE"></span>*Lengua*
</dt> <dd>

Identificador de idioma.

</dd> <dt>

<span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sublanguage*
</dt> <dd>

Identificador de sublenguaje.

</dd> </dl>

Para obtener más información, [vea Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Aceleradores**](accelerators-resource.md)
</dt> <dt>

[**Características**](characteristics-statement.md)
</dt> <dt>

[**Menú**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versión**](version-statement.md)
</dt> </dl>

 

 