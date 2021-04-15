---
title: modificador/sstub
description: El modificador/sstub especifica el nombre del archivo de código auxiliar del servidor para una interfaz RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub modificador MIDL
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676314"
---
# <a name="sstub-switch"></a>modificador/sstub

El modificador **/sstub** especifica el nombre del archivo de código auxiliar del servidor para una interfaz RPC.

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*\_nombre del archivo de código auxiliar \_* 
</dt> <dd>

Especifica un nombre de archivo que invalida el nombre del archivo de código auxiliar del servidor predeterminado. Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El nombre de archivo especificado reemplaza el nombre de archivo predeterminado. De forma predeterminada, el nombre de archivo se obtiene agregando \_ S. C al nombre del archivo IDL. Este modificador no afecta a las interfaces OLE.

Cuando se importan archivos, el nombre de archivo especificado se aplica a un solo archivo de código auxiliar: el archivo de código auxiliar que corresponde al archivo IDL especificado en la línea de comandos.

Si *el \_ \_ nombre del archivo stub* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el modificador [**/out**](-out.md) . Una ruta de acceso explícita en el *\_ \_ nombre de archivo de código auxiliar* invalida la especificación del modificador **/out** .

El modificador none de **/Server** tiene prioridad sobre el modificador **/sstub**

## <a name="examples"></a>Ejemplos

**/sstub MIDL My \_ sstub. c nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




