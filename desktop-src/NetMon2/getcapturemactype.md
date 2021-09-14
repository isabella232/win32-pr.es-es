---
description: La función GetCaptureMacType devuelve el tipo MAC de una captura determinada.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: Función GetCaptureMacType (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171462"
---
# <a name="getcapturemactype-function"></a>Función GetCaptureMacType

La **función GetCaptureMacType** devuelve el tipo MAC de una captura determinada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCapture* \[ En\]
</dt> <dd>

Identificador de la captura. Para obtener información sobre cómo obtener el identificador de captura, vea la sección Comentarios de este **tema GetCaptureMacType.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es uno de los siguientes tipos de MAC.

-   TIPO DE MAC \_ \_ DESCONOCIDO
-   ETHERNET \_ DE TIPO \_ MAC
-   TOKENRING \_ DE \_ TIPO MAC
-   FDDI \_ DE TIPO \_ MAC

Si la función no se realiza correctamente, el valor devuelto es un código de error.



| Código devuelto                                                                                              | Descripción                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**TIPO DE MAC DE NMERR \_ \_ \_ DESCONOCIDO**</dt> </dl> | Monitor de red no se encontró un tipo MAC conocido.<br/> |



 

## <a name="remarks"></a>Observaciones

El identificador de la captura se puede obtener de varias maneras, dependiendo de quién realiza la llamada. Para los expertos, el identificador se especifica en el **miembro hCapture** de la [estructura EXPERTSTARTUPINFO.](expertstartupinfo.md) Para los analizadores, el identificador de captura se puede obtener llamando a la [función GetFrameCaptureHandle.](getframecapturehandle.md)

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetCaptureMacType.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




