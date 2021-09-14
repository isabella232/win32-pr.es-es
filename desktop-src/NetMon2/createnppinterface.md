---
description: La función CreateNPPInterface usa el BLOB devuelto desde el buscador para crear un NPP que la aplicación puede usar.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Función CreateNPPInterface (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253839"
---
# <a name="createnppinterface-function"></a>Función CreateNPPInterface

La **función CreateNPPInterface** usa el BLOB devuelto desde el buscador para crear un NPP que la aplicación puede usar.

## <a name="syntax"></a>Sintaxis


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ En\]
</dt> <dd>

Identificador del BLOB devuelto desde el buscador.

</dd> <dt>

*iid* \[ en\]
</dt> <dd>

Identificador de la interfaz a la que llama desde el NPP **(IRTC** o **IDelaydC,** por ejemplo).

</dd> <dt>

*ppvObject* \[ out\]
</dt> <dd>

Puntero al puntero devuelto a la interfaz solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un valor NMERR que describe el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




