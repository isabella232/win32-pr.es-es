---
description: Obtiene una referencia a un objeto de controlador TCP V4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: ReferenceTcpDriver función)
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
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650161"
---
# <a name="referencetcpdriver-function"></a>ReferenceTcpDriver función)

Obtiene una referencia a un objeto de controlador TCP V4.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDriverObject* \[ enuncia\]
</dt> <dd>

Puntero a una estructura **de \_ objeto de controlador** . Para obtener más información, consulte la documentación del WDK.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve el **estado \_ correcto**. Si se produce un error, devolverá el código de estado adecuado.

## <a name="remarks"></a>Observaciones

Solo se puede llamar a esta función desde el modo kernel. El autor de la llamada debe reducir el recuento de referencias mediante una llamada a la función **ObDereferenceObject** cuando ha terminado con el objeto.

Esta función se implementa en Drvref. lib, que está disponible para su descarga. Vea [biblioteca de API de referencia de controladores de red de Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Drvref. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ReferenceTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 




