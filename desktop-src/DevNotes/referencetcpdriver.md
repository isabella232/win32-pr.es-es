---
description: Obtiene una referencia a un objeto de controlador TCP v4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: Función ReferenceTcpDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 36329ecb695c6fcc011f7e1fe4f44a149fbeac48b0125c34330b9bde51342f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690845"
---
# <a name="referencetcpdriver-function"></a>Función ReferenceTcpDriver

Obtiene una referencia a un objeto de controlador TCP v4.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDriverObject* \[ out\]
</dt> <dd>

Puntero a una **estructura DRIVER \_ OBJECT.** Para más información, consulte la documentación de WDK.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **STATUS \_ SUCCESS**. Si se produce un error, devolverá el código de estado adecuado.

## <a name="remarks"></a>Comentarios

Solo se puede llamar a esta función desde el modo kernel. El autor de la llamada debe disminuir el recuento de referencias llamando a la **función ObDereferenceObject** cuando haya terminado con el objeto .

Esta función se implementa en Drvref.lib, que está disponible para su descarga. Consulte [la Windows API de referencia del controlador de red.](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Drvref.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ReferenceTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 




