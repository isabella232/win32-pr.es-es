---
description: La estructura ENTRYPOINTS define los puntos de entrada a las funciones de exportación que Monitor de red utiliza para operar el analizador.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: Estructura ENTRYPOINTS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000946"
---
# <a name="entrypoints-structure"></a>Estructura ENTRYPOINTS

La estructura **ENTRYPOINTS** define los puntos de entrada a las funciones de exportación que monitor de red utiliza para operar el analizador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Registro**
</dt> <dd>

Puntero a la implementación de la función [*Register Expert*](register-expert.md) .

</dd> <dt>

**Eliminar registro**
</dt> <dd>

Puntero a la implementación de la función de [**eliminación de registro**](deregister.md) .

</dd> <dt>

**RecognizeFrame**
</dt> <dd>

Puntero a la implementación de la función de exportación [**RecognizeFrame**](recognizeframe.md) .

</dd> <dt>

**AttachProperties**
</dt> <dd>

Puntero a la implementación de la función de exportación [**AttachProperties**](attachproperties.md) .

</dd> <dt>

**FormatProperties**
</dt> <dd>

Puntero a la implementación de la función de exportación [**FormatProperties**](formatproperties.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función **CreateProtocol** utiliza la estructura **ENTRYPOINTS** para proporcionar punteros a monitor de red. Los punteros se deben especificar en el orden identificado en la sección de miembros anteriores.

No es necesario implementar la función [**FormatProperties**](formatproperties.md) si monitor de red nunca mostrará los datos del protocolo. Por ejemplo, no es necesario implementar **FormatProperties** si una aplicación de exportación usa la salida del analizador y monitor de red no muestra la salida.



| Para obtener información acerca de                                        | Vea                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red. | [Analizadores](parsers.md)                                  |
| Cómo implementar **DllMain**  incluye un ejemplo.        | [Implementar DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[AttachProperties](attachproperties.md)
</dt> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[Eliminar registro](deregister.md)
</dt> <dt>

[FormatProperties](formatproperties.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> <dt>

[Registro](register-parser.md)
</dt> </dl>

 

 




