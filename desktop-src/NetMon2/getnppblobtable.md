---
description: La función GetNPPBlobTable recupera una tabla BLOB de NPP que representa las NIC de registro en el equipo local.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Función GetNPPBlobTable (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 49920df1be929eb9b35781aeabdcdf47167e82a94066e2d3237207dd00b08f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910705"
---
# <a name="getnppblobtable-function"></a>Función GetNPPBlobTable

La **función GetNPPBlobTable** recupera una tabla BLOB de NPP que representa las NIC de registro en el equipo local.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFilterBlob* \[ En\]
</dt> <dd>

Controle un blob de filtro que limite los blobs de NPP devueltos en la tabla.

</dd> <dt>

*ppBlobTable* \[ out\]
</dt> <dd>

Puntero a una [estructura BLOB \_ TABLE](blob-table.md) que contiene al menos un puntero BLOB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                | Descripción                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ NPP \_ DLL**</dt> </dl>         | No se encontraron archivos DLL en el directorio NPP.<br/>                    |
| <dl> <dt>**NMERR \_ NO HAY DLL DE \_ \_ NPP \_ VÁLIDAS**</dt> </dl> | Ninguno de los archivos DLL del directorio NPP eran archivos DLL de NPP válidos.<br/>  |
| <dl> <dt>**NMERR \_ NO \_ MATCHING \_ NPPS**</dt> </dl>   | Se detectaron blobs de NPP, pero ninguno superó la prueba de filtro.<br/> |
| <dl> <dt>**NMERR \_ OUT \_ OF \_ MEMOR**</dt> </dl>       | Monitor de red no pudo asignar memoria.<br/>            |



 

## <a name="remarks"></a>Comentarios

El BLOB denominado *por hFilterBlob* también puede ser un BLOB especial.

Si establece la marca del blob de filtro en **TRUE,** la tabla BLOB devuelta también puede incluir blobs especiales.

Si el BLOB denominado por *hFilterBlob* es un BLOB especial, Monitor de red interfaz de usuario intentará procesarlo. Por ejemplo, suponga que una llamada anterior devuelve un BLOB especial del NPP remoto. La aplicación inserta la etiqueta necesaria, NOMBRE DE \_ LA MÁQUINA. A continuación, el buscador pasa este BLOB al NPP remoto, que devuelve una tabla de los blobs de NPP asociados al nombre de la máquina.

Para destruir todos los BLOB devueltos y la tabla BLOB, el autor de la llamada es responsable de llamar a la **función DestroyBlob.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




