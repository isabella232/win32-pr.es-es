---
title: Modificador /header
description: El modificador /header especifica el nombre del archivo de encabezado.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- /header switch MIDL
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159754"
---
# <a name="header-switch"></a>Modificador /header

El **modificador /header** especifica el nombre del archivo de encabezado.

``` syntax
midl /header filename
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*filename* 
</dt> <dd>

Especifica un nombre de archivo de encabezado que invalida el nombre de archivo de encabezado predeterminado. Los nombres de archivo se pueden entrecomillar explícitamente mediante comillas dobles (") para evitar que el shell interprete caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El nombre de archivo especificado reemplaza al nombre de archivo predeterminado. El nombre de archivo predeterminado se obtiene reemplazando la extensión de nombre de archivo IDL (normalmente .idl) por la extensión de nombre de archivo .h. Para las interfaces OLE, el **modificador /header** invalida el nombre predeterminado del archivo de encabezado de interfaz.

Al importar archivos, el nombre de archivo especificado solo se aplica a un archivo de encabezado: el archivo de encabezado que corresponde al archivo IDL especificado en la línea de comandos.

Si *filename* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el [**modificador /out.**](-out.md) Una ruta de acceso explícita en *el nombre de* archivo invalida la especificación del modificador **/out.**

## <a name="examples"></a>Ejemplos

**midl /header "bar.h" filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/h**](-h.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> </dl>

 

 




