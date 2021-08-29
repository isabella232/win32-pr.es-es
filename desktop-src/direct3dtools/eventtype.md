---
description: Enumeración que se usa para indicar el tipo de un evento.
MS-HAID: vspixengine.EVENTTYPE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración EVENTTYPE
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7A6F396-5BC0-4963-ABFD-ACB7AAE475F5
api_name:
- EVENTTYPE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: daa61cc8358fb0dc59f4b819e27077c68748b995
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624441"
---
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span id="vspixengine.eventtype"></span>Enumeración EVENTTYPE

Enumeración que se usa para indicar el tipo de un evento.

## <a name="syntax"></a>Sintaxis

```cpp
C++ 
enum EVENTTYPE {
  ET_NONE = 0, 
  ET_SESSIONSTART, 
  ET_SESSIONEND, 
  ET_PROCESSSTART, 
  ET_PROCESSEND, 
  ET_FRAMEBEGIN, 
  ET_FRAMEEND, 
  ET_USEREVENTBEGIN, 
  ET_USEREVENTEND, 
  ET_USERMARKER, 
  ET_CALL, 
  ET_OBJECTCREATION, 
  ET_OBJECTPOPULATION, 
  ET_CALLSYNC, 
  ET_DRAW, 
  ET_DISPATCH 
};
```

## <a name="constants"></a>Constantes

<span id="ET_NONE"></span><span id="et_none"></span>**ET \_ NONE**  
Valor que corresponde a ningún evento.

<span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**ET \_ SESSIONSTART**  
Valor que corresponde a un evento de inicio de sesión.

<span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**ET \_ SESSIONEND**  
Valor que corresponde a un evento de fin de sesión.

<span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET \_ PROCESSSTART**  
Valor que corresponde a un evento de inicio del proceso.

<span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET \_ PROCESSEND**  
Valor que corresponde a un evento de finalización del proceso.

<span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**ET \_ FRAMEBEGIN**  
Valor que corresponde a un evento de inicio de fotograma.

<span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**ET \_ FRAMEEND**  
Valor que corresponde a un evento de extremo de fotograma. No se utiliza.

<span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET \_ USEREVENTBEGIN**  
Valor que corresponde a un evento begin de evento de usuario.

<span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET \_ USEREVENTEND**  
Valor que corresponde a un evento final de evento de usuario. No se utiliza.

<span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**ET \_ USERMARKER**  
Valor que corresponde a un evento de marcador de usuario.

<span id="ET_CALL"></span><span id="et_call"></span>**ET \_ CALL**  
Valor que corresponde a un evento de llamada.

<span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET \_ OBJECTCREATION**  
Valor que corresponde a un evento de creación de objetos.

<span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET \_ OBJECTPOPULATION**  
Valor que corresponde a un evento de población de objetos.

<span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET \_ CALLSYNC**  

<span id="ET_DRAW"></span><span id="et_draw"></span>**ET \_ DRAW**  
Valor que corresponde a un evento de llamada a draw.

<span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**ET \_ DISPATCH**  
Valor que corresponde a un evento de distribución.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>
