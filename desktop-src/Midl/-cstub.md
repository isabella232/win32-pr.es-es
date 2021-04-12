---
title: modificador/cstub
description: El modificador/cstub especifica el nombre del archivo de código auxiliar de cliente para una interfaz RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub modificador MIDL
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358246"
---
# <a name="cstub-switch"></a>modificador/cstub

El modificador **/cstub** especifica el nombre del archivo de código auxiliar de cliente para una interfaz RPC.

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*\_nombre del archivo de código auxiliar \_* 
</dt> <dd>

Especifica un nombre de archivo que invalida el nombre del archivo de código auxiliar de cliente predeterminado. Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El nombre de archivo especificado reemplaza el nombre de archivo predeterminado. De forma predeterminada, el nombre de archivo se obtiene agregando la extensión \_ c. c al nombre del archivo IDL. Este modificador no afecta a las interfaces OLE.

Cuando se importan archivos, el nombre de archivo especificado se aplica a un solo archivo de código auxiliar: el archivo de código auxiliar que corresponde al archivo IDL especificado en la línea de comandos.

Si *el \_ \_ nombre del archivo stub* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el modificador [**/out**](-out.md) . Una ruta de acceso explícita en el *\_ \_ nombre de archivo de código auxiliar* invalida la especificación del modificador **/out** .

El modificador **/Client** no tiene prioridad sobre el modificador **/cstub**

## <a name="examples"></a>Ejemplos

**/cstub MIDL My \_ cstub. c nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/header**](-header.md)
</dt> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




