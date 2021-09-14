---
title: Modificador /acf
description: El modificador /acf permite al usuario proporcionar un nombre de archivo ACF explícito. El modificador también permite el uso de diferentes nombres de interfaz en los archivos IDL y ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /acf switch MIDL
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159779"
---
# <a name="acf-switch"></a>Modificador /acf

El **modificador /acf** permite al usuario proporcionar un nombre de archivo ACF explícito. El modificador también permite el uso de diferentes nombres de interfaz en los archivos IDL y ACF.

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*acf \_ filename* 
</dt> <dd>

Especifica el nombre del ACF. El espacio en blanco puede estar presente o no entre el **modificador /acf** y el nombre de archivo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

De forma predeterminada, el compilador MIDL construye el nombre de ACF reemplazando la extensión de nombre de archivo IDL (normalmente .idl) por .acf. Cuando el **modificador /acf** está presente, el ACF toma su nombre del nombre de archivo especificado. El **modificador /acf** solo se aplica al archivo IDL especificado en la línea de comandos del compilador midl. No se aplica a los archivos importados.

Cuando se **usa el modificador /acf,** el nombre de interfaz del ACF no tiene que coincidir con el nombre de la interfaz MIDL. Esta característica permite que las interfaces compartan una especificación de ACF.

Cuando no se especifica una ruta de acceso absoluta a un ACF, el compilador MIDL busca en el directorio actual, directorios proporcionados por la opción [**/I**](-i.md) y directorios en la ruta de acceso INCLUDE.

Si no se encuentra el ACF, el compilador de MIDL asume que no hay ACF para esta interfaz. Para obtener más información sobre la secuencia de directorios, vea las entradas de referencia para los modificadores [**/I**](-i.md) y [**/no \_ def \_ idir.**](-no-def-idir.md) Para obtener más información relacionada con **/acf,** vea Archivo de [definición de interfaz (IDL).](interface-definition-idl-file.md)

## <a name="examples"></a>Ejemplos

**midl /acf bar.acf filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**/I**](-i.md)
</dt> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 




