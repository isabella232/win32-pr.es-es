---
description: La función register export debe implementarse en todos los archivos DLL del analizador. La implementación de Register crea y rellena una base de datos de propiedades para un protocolo. Monitor de red la base de datos para determinar qué propiedades admite el protocolo.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Registrar función de devolución de llamada del analizador (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074095"
---
# <a name="register-parser-callback-function"></a>Registrar función de devolución de llamada del analizador

La **función register** export debe implementarse en todos los archivos DLL del analizador. La implementación de **Register crea** y rellena una base de datos de [*propiedades*](p.md) para un protocolo. Monitor de red la base de datos para determinar qué propiedades admite el protocolo.

## <a name="syntax"></a>Sintaxis


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ En\]
</dt> <dd>

Identificador del protocolo que Monitor de red al llamar a **Register**. El *identificador hProtocol* es necesario al llamar a las funciones auxiliares de exportación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno.

## <a name="remarks"></a>Observaciones

Monitor de red llama a la **función Register** en cuanto se carga una captura. Monitor de red llama a **la función Register** para cada protocolo que pueda identificar. La [función CreateProtocol](createprotocol.md) pasa un puntero a la **función Register.**

La implementación de **Register** incluye llamadas a las siguientes funciones.

-   Una llamada a las [funciones CreatePropertyDatabase](createpropertydatabase.md) y [AddProperty](/previous-versions/bb251873(v=msdn.10)) para crear una base de datos de todas las propiedades que admite el protocolo.
-   Se requiere una llamada a [la función CreateHandoffTable](createhandofftable.md) si el protocolo usa un [*conjunto de entrega.*](h.md)

Si el archivo DLL del analizador contiene varios analizadores y el analizador puede detectar más de un protocolo, debe implementar una función **Register** para cada protocolo.



| Para obtener información sobre                                        | Vea                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                 |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.        | [Arquitectura dll del analizador](parser-dll-architecture.md) |
| La implementación de **Register**  incluye un ejemplo.       | [Implementar el registro](implementing-register.md)     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> <dt>

[CreatePropertyDatabase](createpropertydatabase.md)
</dt> <dt>

[CreateProtocol](createprotocol.md)
</dt> </dl>

 

