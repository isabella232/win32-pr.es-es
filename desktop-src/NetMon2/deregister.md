---
description: La función Deregister export libera los recursos usados para crear la base de datos de propiedades de protocolo. El archivo DLL del analizador debe implementar Deregister.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Anular el registro de la función de devolución de llamada (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260503"
---
# <a name="deregister-callback-function"></a>Anular el registro de la función de devolución de llamada

La **función Deregister** export libera los recursos usados para crear la base de datos de [*propiedades de protocolo*](p.md). El archivo DLL del analizador debe implementar **Deregister**.

## <a name="syntax"></a>Sintaxis


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ En\]
</dt> <dd>

Identificador del protocolo para una base de datos específica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno.

## <a name="remarks"></a>Observaciones

Monitor de red llama a **Deregister después** de pasar toda la información de captura al archivo DLL del analizador. El archivo DLL del analizador debe implementar una **función Deregister** para cada protocolo que admita el analizador.

Al implementar **Deregister**, el archivo DLL del analizador debe llamar a la [función DestroyPropertyDatabase](destroypropertydatabase.md) para liberar los recursos de la base [*de datos de*](p.md) propiedades.



| Para obtener información acerca de                                        | Vea                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                 |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.        | [Arquitectura dll del analizador](parser-dll-architecture.md) |
| La implementación de **Deregister incluye**  un ejemplo.     | [Implementación de Anulación del registro](implementing-deregister.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DestroyPropertyDatabase](destroypropertydatabase.md)
</dt> </dl>

 

 




