---
description: Recupera el tipo MAC de la categoría NetworkInfo de la sección NPP del BLOB y convierte los datos de tipo en un número de tipo MAC.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Función GetNPPMacTypeAsNumber (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476754"
---
# <a name="getnppmactypeasnumber-function"></a>Función GetNPPMacTypeAsNumber

La **función GetNPPMacTypeAsNumber** recupera el tipo MAC de la categoría NetworkInfo de la sección NPP del BLOB y convierte los datos de tipo en un número de tipo MAC.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ En\]
</dt> <dd>

Identificador del BLOB especificado.

</dd> <dt>

*lpMacType* \[ out\]
</dt> <dd>

Puntero al tipo MAC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la etiqueta no está disponible, el valor devuelto es MAC \_ TYPE \_ UNKNOWN.

## <a name="remarks"></a>Observaciones

Esta función asigna la etiqueta **NPP:NetworkInfo:MacType** al **\_ \_ \* tipo de MAC** tal como se define en el archivo Npptypes.h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




