---
title: modificador/header
description: El modificador/header especifica el nombre del archivo de encabezado.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- /header modificador MIDL
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419650"
---
# <a name="header-switch"></a>modificador/header

El modificador **/Header** especifica el nombre del archivo de encabezado.

``` syntax
midl /header filename
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*filename* 
</dt> <dd>

Especifica un nombre de archivo de encabezado que invalida el nombre de archivo de encabezado predeterminado. Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El nombre de archivo especificado reemplaza el nombre de archivo predeterminado. El nombre de archivo predeterminado se obtiene reemplazando la extensión de nombre de archivo IDL (normalmente,. idl) por la extensión de nombre de archivo. h. En el caso de las interfaces OLE, el modificador **/Header** invalida el nombre predeterminado del archivo de encabezado de interfaz.

Cuando se importan archivos, el nombre de archivo especificado se aplica a un solo archivo de encabezado: el archivo de encabezado que corresponde al archivo IDL especificado en la línea de comandos.

Si *filename* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el modificador [**/out**](-out.md) . Una ruta de acceso explícita en *filename* invalida la especificación del modificador **/out** .

## <a name="examples"></a>Ejemplos

**MIDL/header "bar. h" nombreDeArchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
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

 

 




