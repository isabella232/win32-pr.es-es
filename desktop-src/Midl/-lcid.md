---
title: /LCID (modificador)
description: La opción del compilador/LCID MIDL permite usar caracteres internacionales en los archivos de entrada, nombres de archivo y rutas de acceso de directorio.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /LCID (modificador) MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358243"
---
# <a name="lcid-switch"></a>/LCID (modificador)

La opción del compilador **/LCID** MIDL permite usar caracteres internacionales en los archivos de entrada, nombres de archivo y rutas de acceso de directorio.

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*LCID* 
</dt> <dd>

Especifica el identificador de configuración regional de 32 bits usado en la compatibilidad con el idioma nacional de Windows. El identificador de configuración regional debe especificarse en formato decimal.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Dentro de los archivos de entrada, puede usar los comentarios, las cadenas, los helpstrings y los identificadores localizados. En concreto, el modificador **/LCID** proporciona compatibilidad completa con DBCS, para representar idiomas asiáticos como japonés, Chino y coreano.

> [!Note]  
> El modificador **/LCID** está disponible con la versión 3.01.75 de MIDL y versiones posteriores.

 

## <a name="examples"></a>Ejemplos

**MIDL/LCID 1041 iFace. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> </dl>

 

 




