---
title: Modificador /cstub
description: El modificador /cstub especifica el nombre del archivo de código auxiliar de cliente para una interfaz RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub switch MIDL
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b4f635b6d09c85b345eea6dcb7320294e226ad6f2540f01af1e9b3e8098671
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105665"
---
# <a name="cstub-switch"></a>Modificador /cstub

El **modificador /cstub** especifica el nombre del archivo de código auxiliar de cliente para una interfaz RPC.

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*nombre de \_ archivo \_ de código auxiliar* 
</dt> <dd>

Especifica un nombre de archivo que invalida el nombre de archivo de código auxiliar de cliente predeterminado. Los nombres de archivo se pueden entrecomillar explícitamente mediante comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El nombre de archivo especificado reemplaza el nombre de archivo predeterminado. De forma predeterminada, el nombre de archivo se obtiene agregando la \_ extensión c.c al nombre del archivo IDL. Este modificador no afecta a las interfaces OLE.

Al importar archivos, el nombre de archivo especificado solo se aplica a un archivo de código auxiliar, el archivo de código auxiliar que corresponde al archivo IDL especificado en la línea de comandos.

Si *el nombre del archivo \_ \_ de* código auxiliar no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el [**modificador /out.**](-out.md) Una ruta de acceso explícita en *el nombre de archivo de \_ \_ código* auxiliar invalida la especificación del modificador **/out.**

El **modificador /client** none tiene prioridad sobre **el modificador /cstub.**

## <a name="examples"></a>Ejemplos

**midl /cstub my \_ cstub.c filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/header**](-header.md)
</dt> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




