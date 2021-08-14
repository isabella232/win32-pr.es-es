---
title: Modificador /lcid
description: La opción del compilador /lcid MIDL permite usar caracteres internacionales en los archivos de entrada, los nombres de archivo y las rutas de acceso de directorio.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /lcid switch MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ceff1f9a4ef2f6c95a8dac12ff689995efe4fdd3619cf48e11043967fec053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385518"
---
# <a name="lcid-switch"></a>Modificador /lcid

La **opción del compilador /lcid** MIDL permite usar caracteres internacionales en los archivos de entrada, los nombres de archivo y las rutas de acceso de directorio.

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*localeID* 
</dt> <dd>

Especifica el identificador de configuración regional de 32 bits que se usa Windows compatibilidad con idiomas nacionales. El identificador de configuración regional debe especificarse en decimal.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Dentro de los archivos de entrada, puede usar comentarios localizados, cadenas, cadenas de ayuda e identificadores. En concreto, el **modificador /lcid** proporciona compatibilidad completa con DBCS para representar idiomas asiáticos como japonés, chino y coreano.

> [!Note]  
> El **modificador /lcid** está disponible con MIDL versión 3.01.75 y posteriores.

 

## <a name="examples"></a>Ejemplos

**midl /lcid 1041 iface.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> </dl>

 

 




