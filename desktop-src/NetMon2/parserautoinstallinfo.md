---
description: La función de exportación ParserAutoInstallInfo identifica el analizador o los analizadores que se encuentran en un archivo DLL. ParserAutoInstallInfo debe implementarse en todos los archivos dll de analizador.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Función de devolución de llamada ParserAutoInstallInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360147"
---
# <a name="parserautoinstallinfo-callback-function"></a>Función de devolución de llamada ParserAutoInstallInfo

La función de exportación **ParserAutoInstallInfo** identifica el analizador o los analizadores que se encuentran en un archivo dll. **ParserAutoInstallInfo** debe implementarse en todos los archivos dll de analizador.

## <a name="syntax"></a>Sintaxis


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a>Parámetros

Esta función de devolución de llamada no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es una estructura [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) que describe los analizadores en el archivo dll.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Cuando Monitor de red se carga por primera vez, llama a **ParserAutoInstallInfo** (si existe) para instalar automáticamente cada analizador y, a continuación, enumera todos los archivos DLL del analizador en el subdirectorio del analizador.

La información devuelta en la estructura **PF \_ PARSERDLLINFO** incluye lo siguiente:

-   El número de analizadores en el archivo DLL (normalmente uno).
-   El nombre y una breve descripción del protocolo que detecta cada analizador.
-   Un archivo de ayuda opcional para cada protocolo.
-   Los protocolos que preceden a cada protocolo.
-   Los protocolos que siguen a cada protocolo.

Cada DLL del analizador debe contener un analizador. Sin embargo, Monitor de red le permite crear un archivo DLL que contiene más de un analizador. Por ejemplo, tcpip.dll es una Monitor de red DLL con más de un analizador.



| Para obtener información acerca de                                               | Vea                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.        | [Analizadores](parsers.md)                                                       |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.               | [Arquitectura de DLL de analizador](parser-dll-architecture.md)                       |
| Cómo implementar **ParserAutoInstallInfo**  incluye un ejemplo. | [Implementación de ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




