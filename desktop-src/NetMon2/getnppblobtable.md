---
description: La función GetNPPBlobTable recupera una tabla BLOB NPP que representa las NIC de registro del equipo local.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Función GetNPPBlobTable (Netmon. h)
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
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910885"
---
# <a name="getnppblobtable-function"></a>GetNPPBlobTable función)

La función **GetNPPBlobTable** recupera una tabla BLOB NPP que representa las NIC de registro del equipo local.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFilterBlob* \[ de\]
</dt> <dd>

Identificador de un BLOB en filtro que limita los blobs NPP devueltos en la tabla.

</dd> <dt>

*ppBlobTable* \[ enuncia\]
</dt> <dd>

Puntero a una estructura de [ \_ tabla de BLOB](blob-table.md) que contiene al menos un puntero de BLOB.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                | Descripción                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ hay \_ dll NPP**</dt> </dl>         | No se encontró ningún dll en el directorio NPP.<br/>                    |
| <dl> <dt>**NMERR \_ no hay ningún \_ \_ dll NPP válido \_**</dt> </dl> | Ninguno de los archivos DLL del directorio NPP eran archivos dll NPP válidos.<br/>  |
| <dl> <dt>**NMERR \_ no \_ \_ NPPS coincidente**</dt> </dl>   | Se detectaron blobs NPP, pero ninguno pasó la prueba de filtro.<br/> |
| <dl> <dt>**NMERR \_ fuera \_ del \_ memorando**</dt> </dl>       | Monitor de red no pudo asignar memoria.<br/>            |



 

## <a name="remarks"></a>Observaciones

El BLOB denominado por *hFilterBlob* también puede ser un BLOB especial.

Si establece la marca en el BLOB de filtro en **true**, la tabla BLOB devuelta también puede incluir blobs especiales.

Si el BLOB llamado por *hFilterBlob* es un BLOB especial, la interfaz de usuario de monitor de red intentará procesarlo. Por ejemplo, supongamos que una llamada anterior devuelve un BLOB especial del NPP remoto. La aplicación inserta la etiqueta necesaria, el nombre de la máquina \_ . A continuación, el buscador pasa este BLOB al NPP remoto, que luego devuelve una tabla de los blobs NPP asociados al nombre de la máquina.

Para destruir todos los blobs devueltos y la tabla BLOB, el autor de la llamada es responsable de llamar a la función **DestroyBlob** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




