---
description: Obtiene una referencia a un objeto de controlador de TCP V6.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: ReferenceTcpDriverV6 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650131"
---
# <a name="referencetcpdriverv6-function"></a>ReferenceTcpDriverV6 función)

Obtiene una referencia a un objeto de controlador de TCP V6.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
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

[**ReferenceTcpDriver**](referencetcpdriver.md)
</dt> </dl>

 

 




