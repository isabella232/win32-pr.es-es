---
description: Cierra el administrador de OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: OcTerminate función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649649"
---
# <a name="octerminate-function"></a>OcTerminate función)

Cierra el administrador de OC.

## <a name="syntax"></a>Sintaxis


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OcManagerContext* \[ in, out\]
</dt> <dd>

En la entrada, contiene el puntero de contexto del administrador de OC devuelto por [**OcInitialize**](ocinitialize.md). En la salida, recibe **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**OcInitialize**](ocinitialize.md)
</dt> </dl>

 

 
