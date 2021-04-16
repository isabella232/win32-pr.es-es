---
description: La función de exportación de registros debe implementarse en todos los archivos dll de analizador. La implementación de Register crea y rellena en una base de datos de propiedades para un protocolo. Monitor de red usa la base de datos para determinar las propiedades que admite el protocolo.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Función de devolución de llamada del analizador de registro (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677642"
---
# <a name="register-parser-callback-function"></a>Registrar función de devolución de llamada del analizador

La función de exportación de **registros** debe implementarse en todos los archivos dll de analizador. La implementación de **Register** crea y rellena en una base de [*datos de propiedades*](p.md) para un protocolo. Monitor de red usa la base de datos para determinar las propiedades que admite el protocolo.

## <a name="syntax"></a>Sintaxis


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ de\]
</dt> <dd>

Identificador del protocolo que Monitor de red proporciona al llamar a **Register**. El identificador *hProtocol* es necesario cuando se llama a funciones auxiliares de exportación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno.

## <a name="remarks"></a>Observaciones

Monitor de red comienza a llamar a la función **Register** en cuanto se carga una captura. Monitor de red llama a la función de **registro** para cada protocolo que puede identificar. La función [CreateProtocol](createprotocol.md) pasa un puntero a la función de **registro** .

La implementación de **Register** incluye llamadas a las siguientes funciones.

-   Una llamada a las funciones [CreatePropertyDatabase](createpropertydatabase.md) y [AddProperty](/previous-versions/bb251873(v=msdn.10)) para crear una base de datos de todas las propiedades que admite el protocolo.
-   Se requiere una llamada a la función [CreateHandoffTable](createhandofftable.md) si el protocolo utiliza un [*conjunto de entrega*](h.md).

Si el archivo DLL del analizador contiene varios analizadores y el analizador puede detectar más de un protocolo, debe implementar una función de **registro** para cada protocolo.



| Para obtener información sobre                                        | Vea                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                 |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.        | [Arquitectura de DLL de analizador](parser-dll-architecture.md) |
| Cómo implementar **el registro**  incluye un ejemplo.       | [Implementación del registro](implementing-register.md)     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[CreateHandoffTable](createhandofftable.md)
</dt> <dt>

[CreatePropertyDatabase](createpropertydatabase.md)
</dt> <dt>

[CreateProtocol](createprotocol.md)
</dt> </dl>

 

