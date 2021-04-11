---
description: La función de Desregistro de exportación libera los recursos usados para crear la base de datos de propiedades de protocolo. El archivo DLL del analizador debe implementar Unregister.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Anular el registro de la función de devolución de llamada (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276695"
---
# <a name="deregister-callback-function"></a>Anular la función de devolución de llamada

La función de **Desregistro** de exportación libera los recursos usados para crear la [*base de datos de propiedades*](p.md)de protocolo. El archivo DLL del analizador debe implementar **unregister**.

## <a name="syntax"></a>Sintaxis


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProtocol* \[ de\]
</dt> <dd>

Identificador del protocolo para una base de datos específica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno.

## <a name="remarks"></a>Observaciones

Monitor de red llama a **anular registro** después de pasar toda la información de captura a la dll del analizador. El archivo DLL del analizador debe implementar una función de **eliminación de registro** para cada protocolo que admita el analizador.

Al implementar **unregister**, el archivo DLL del analizador debe llamar a la función [DestroyPropertyDatabase](destroypropertydatabase.md) para liberar los recursos de la [*base de datos de propiedades*](p.md) .



| Para obtener información acerca de                                        | Vea                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                 |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.        | [Arquitectura de DLL de analizador](parser-dll-architecture.md) |
| Cómo implementar **unregister**  incluye un ejemplo.     | [Implementación de unregister](implementing-deregister.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DestroyPropertyDatabase](destroypropertydatabase.md)
</dt> </dl>

 

 




