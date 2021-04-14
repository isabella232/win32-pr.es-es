---
title: LANGUAGE (instrucción)
description: Define el idioma de todos los recursos hasta la siguiente instrucción de lenguaje o hasta el final del archivo.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Menús de instrucciones de lenguaje y otros recursos
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533166"
---
# <a name="language-statement"></a>LANGUAGE (instrucción)

Define el idioma de todos los recursos hasta la siguiente instrucción de **lenguaje** o hasta el final del archivo.

Cuando la instrucción del **lenguaje** aparece antes del principio del cuerpo de una definición de recursos [**Accelerators**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**Menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**stringtable**](stringtable-resource.md) , el idioma especificado solo se aplica a ese recurso.

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span id="language"></span><span id="LANGUAGE"></span>*módulo*
</dt> <dd>

Identificador de idioma.

</dd> <dt>

<span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*subidioma*
</dt> <dd>

Identificador de subidioma.

</dd> </dl>

Para obtener más información, vea [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**SUS**](characteristics-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versión**](version-statement.md)
</dt> </dl>

 

 