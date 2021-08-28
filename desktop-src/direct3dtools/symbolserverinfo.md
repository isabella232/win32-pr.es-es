---
description: Representa información sobre el servidor de símbolos de depuración.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura SymbolServerInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 28f85445e6affc006c5c0898df1c85d71693a66d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632093"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>Estructura SymbolServerInfo

Representa información sobre el servidor de símbolos de depuración.

## <a name="syntax"></a>Sintaxis


```C++
} SymbolServerInfo;
```

## <a name="members"></a>Miembros

**symbolPath**  
Cadena COM que contiene la ruta de acceso del servidor de símbolos.

**symbolCacheDir**  
Cadena COM que contiene el directorio de caché del servidor de símbolos.

**publicSymbolServerName**  
Cadena COM que contiene el nombre público del servidor de símbolos.

**symbolExcludeList**  
Cadena COM que especifica la lista de símbolos que se excluirán.

**symbolIncludeList**  
Cadena COM que especifica la lista de símbolos que se incluirán.

**useExcludeList**  
True si se omite la lista de exclusión; de lo contrario, false.

**useMSSymbolServer**  
true si se usa el servidor de símbolos de Microsoft; de lo contrario, false.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



