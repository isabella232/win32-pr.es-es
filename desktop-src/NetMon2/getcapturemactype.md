---
description: La función GetCaptureMacType devuelve el tipo MAC de una captura determinada.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: Función GetCaptureMacType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808720"
---
# <a name="getcapturemactype-function"></a>GetCaptureMacType función)

La función **GetCaptureMacType** devuelve el tipo Mac de una captura determinada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCapture* \[ de\]
</dt> <dd>

Identificador de la captura. Para obtener información sobre cómo obtener el identificador de captura, vea la sección Comentarios de este tema **GetCaptureMacType** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es uno de los siguientes tipos de MAC.

-   tipo de MAC \_ \_ desconocido
-   \_Ethernet de tipo Mac \_
-   \_TOKENRING de tipo Mac \_
-   \_FDDI de tipo Mac \_

Si la función no es correcta, el valor devuelto es un código de error.



| Código devuelto                                                                                              | Descripción                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_tipo de Mac NMERR \_ \_ desconocido**</dt> </dl> | Monitor de red no encontró un tipo de MAC conocido.<br/> |



 

## <a name="remarks"></a>Observaciones

El identificador de la captura se puede obtener de varias maneras, en función de quién realice la llamada. En el caso de los expertos, el identificador se especifica en el miembro **hCapture** de la estructura [EXPERTSTARTUPINFO](expertstartupinfo.md) . En el caso de los analizadores, el identificador de captura se puede obtener llamando a la función [GetFrameCaptureHandle](getframecapturehandle.md) .

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetCaptureMacType** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




