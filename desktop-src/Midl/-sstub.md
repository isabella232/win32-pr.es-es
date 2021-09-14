---
title: Modificador /sstub
description: El modificador /sstub especifica el nombre del archivo de código auxiliar del servidor para una interfaz RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub switch MIDL
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159705"
---
# <a name="sstub-switch"></a>Modificador /sstub

El **modificador /sstub** especifica el nombre del archivo de código auxiliar del servidor para una interfaz RPC.

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*nombre de \_ archivo \_ de código auxiliar* 
</dt> <dd>

Especifica un nombre de archivo que invalida el nombre de archivo de código auxiliar del servidor predeterminado. Los nombres de archivo se pueden entrecomillar explícitamente mediante comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El nombre de archivo especificado reemplaza el nombre de archivo predeterminado. De forma predeterminada, el nombre de archivo se obtiene \_ agregando S.C al nombre del archivo IDL. Este modificador no afecta a las interfaces OLE.

Al importar archivos, el nombre de archivo especificado solo se aplica a un archivo de código auxiliar, el archivo de código auxiliar que corresponde al archivo IDL especificado en la línea de comandos.

Si *el nombre del archivo \_ \_ de* código auxiliar no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el [**modificador /out.**](-out.md) Una ruta de acceso explícita en *el nombre de archivo de \_ \_ código* auxiliar invalida la especificación del modificador **/out.**

El **modificador /server** none tiene prioridad sobre **el modificador /sstub.**

## <a name="examples"></a>Ejemplos

**midl /sstub my \_ sstub.c filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




