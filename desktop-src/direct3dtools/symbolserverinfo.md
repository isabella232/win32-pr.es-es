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
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152214"
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
Cadena COM que especifica la lista de símbolos que se van a excluir.

**symbolIncludeList**  
Cadena COM que especifica la lista de símbolos que se van a incluir.

**useExcludeList**  
True si se omite la lista de exclusión; en caso contrario, false.

**useMSSymbolServer**  
True si se usa el servidor de símbolos de Microsoft; en caso contrario, false.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



