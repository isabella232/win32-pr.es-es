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
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159746"
---
# <a name="lcid-switch"></a>Modificador /lcid

La **opción del compilador /lcid** MIDL permite usar caracteres internacionales en los archivos de entrada, los nombres de archivo y las rutas de acceso de directorio.

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*localeID* 
</dt> <dd>

Especifica el identificador de configuración regional de 32 bits que se usa Windows compatibilidad con idiomas nacionales. El identificador de configuración regional debe especificarse en decimal.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Dentro de los archivos de entrada, puede usar comentarios localizados, cadenas, cadenas de ayuda e identificadores. En concreto, el **modificador /lcid** proporciona compatibilidad completa con DBCS, para representar idiomas asiáticos como japonés, chino y coreano.

> [!Note]  
> El **modificador /lcid** está disponible con midl versión 3.01.75 y versiones posteriores.

 

## <a name="examples"></a>Ejemplos

**midl /lcid 1041 iface.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> </dl>

 

 




