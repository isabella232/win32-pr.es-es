---
title: modificador/ACF
description: El modificador/ACF permite al usuario proporcionar un nombre de archivo ACF explícito. El modificador también permite el uso de diferentes nombres de interfaz en los archivos IDL y ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /ACF modificador MIDL
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994753"
---
# <a name="acf-switch"></a>modificador/ACF

El modificador **/ACF** permite al usuario proporcionar un nombre de archivo ACF explícito. El modificador también permite el uso de diferentes nombres de interfaz en los archivos IDL y ACF.

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*\_archivo ACF* 
</dt> <dd>

Especifica el nombre del ACF. El espacio en blanco puede estar o no estar presente entre el modificador **/ACF** y el nombre de archivo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

De forma predeterminada, el compilador MIDL crea el nombre de ACF reemplazando la extensión de nombre de archivo IDL (normalmente. idl) por. ACF. Cuando el modificador **/ACF** está presente, el ACF toma el nombre del nombre de archivo especificado. El modificador **/ACF** solo se aplica al archivo IDL especificado en la línea de comandos del compilador MIDL. No se aplica a los archivos importados.

Cuando se usa el modificador **/ACF** , no es necesario que el nombre de la interfaz de ACF coincida con el nombre de la interfaz MIDL. Esta característica permite a las interfaces compartir una especificación ACF.

Cuando no se especifica una ruta de acceso absoluta a un ACF, el compilador MIDL busca en el directorio actual, en los directorios proporcionados por la opción [**/i**](-i.md) y en los directorios de la ruta de acceso de inclusión.

Si no se encuentra el ACF, el compilador MIDL supone que no hay ningún ACF para esta interfaz. Para obtener más información acerca de la secuencia de directorios, consulte las entradas de referencia de los modificadores [**/i**](-i.md) y [**/no \_ Def \_ Idir**](-no-def-idir.md) Para obtener más información relacionada con **/ACF**, vea [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Ejemplos

**MIDL/ACF bar. ACF nombreDeArchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/I**](-i.md)
</dt> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ Def \_ Idir**](-no-def-idir.md)
</dt> </dl>

 

 




