---
description: Recupera el tipo MAC de la categoría NetworkInfo de la sección NPP del BLOB y convierte los datos de tipo en un número de tipo MAC.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Función GetNPPMacTypeAsNumber (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540203"
---
# <a name="getnppmactypeasnumber-function"></a>GetNPPMacTypeAsNumber función)

La función **GetNPPMacTypeAsNumber** recupera el tipo Mac de la categoría NetworkInfo de la sección NPP del BLOB y convierte los datos de tipo en un número de tipo Mac.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ de\]
</dt> <dd>

Identificador del BLOB especificado.

</dd> <dt>

*lpMacType* \[ enuncia\]
</dt> <dd>

Un puntero al tipo MAC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la etiqueta no está disponible, el valor devuelto es de \_ tipo Mac \_ desconocido.

## <a name="remarks"></a>Observaciones

Esta función asigna la etiqueta, **NPP: NetworkInfo: MacType** al **\_ \_ \* tipo Mac** tal y como se define en el archivo Npptypes. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




