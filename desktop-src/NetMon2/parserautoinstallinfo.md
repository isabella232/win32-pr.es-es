---
description: La función de exportación ParserAutoInstallInfo identifica el analizador o los analizadores que se encuentran en un archivo DLL. ParserAutoInstallInfo debe implementarse en todos los archivos DLL del analizador.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Función de devolución de llamada ParserAutoInstallInfo (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074113"
---
# <a name="parserautoinstallinfo-callback-function"></a>Función de devolución de llamada ParserAutoInstallInfo

La función de **exportación ParserAutoInstallInfo** identifica el analizador o los analizadores que se encuentran en un archivo DLL. **ParserAutoInstallInfo** debe implementarse en todos los archivos DLL del analizador.

## <a name="syntax"></a>Sintaxis


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a>Parámetros

Esta función de devolución de llamada no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es una estructura [ \_ PF PARSERDLLINFO](pf-parserdllinfo.md) que describe los analizadores del archivo DLL.

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Observaciones

Cuando Monitor de red carga por primera vez, llama a **ParserAutoInstallInfo** (si existe) para instalar automáticamente cada analizador y, a continuación, enumera todos los archivos DLL del analizador en el subdirectorio del analizador.

La información devuelta en la **\_ estructura PF PARSERDLLINFO** incluye lo siguiente:

-   Número de analizadores del archivo DLL (normalmente uno).
-   Nombre y una breve descripción del protocolo que detecta cada analizador.
-   Un archivo de Ayuda opcional para cada protocolo.
-   Protocolos que preceden a cada protocolo.
-   Los protocolos que siguen a cada protocolo.

Cada archivo DLL del analizador debe contener un analizador. Sin embargo, Monitor de red permite crear un archivo DLL que contiene más de un analizador. Por ejemplo, tcpip.dll es un Monitor de red DLL con más de un analizador.



| Para obtener información acerca de                                               | Vea                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.        | [Analizadores](parsers.md)                                                       |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.               | [Arquitectura dll del analizador](parser-dll-architecture.md)                       |
| Cómo implementar **ParserAutoInstallInfo incluye**  un ejemplo. | [Implementación de ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




