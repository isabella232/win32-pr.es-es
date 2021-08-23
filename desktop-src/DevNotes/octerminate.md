---
description: Cierra el administrador de OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: Función OcTerminate
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
ms.openlocfilehash: 399bdb936befb4f7ff45f9f5a3b132245b984bf2a5201ce054ee0fbeb50f5598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833355"
---
# <a name="octerminate-function"></a>Función OcTerminate

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

En la entrada, contiene el puntero de contexto del administrador de OC devuelto [**por OcInitialize**](ocinitialize.md). En la salida, recibe **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**OcInitialize**](ocinitialize.md)
</dt> </dl>

 

 
