---
description: 'Más información sobre: WCHAR'
title: WCHAR
TOCTitle: WCHAR
ms:assetid: 922431b3-bf9a-4aba-bc67-dd33d9aeaac0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269344(v=EXCHG.10)
ms:contentKeyID: 32765633
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8888b1c270ae670453f4dd09579f1eae12c09486
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477411"
---
# <a name="wchar"></a>WCHAR


_**Se aplica a:** Windows | Windows Servidor_

## <a name="wchar"></a>WCHAR

El tipo de datos WCHAR contiene un carácter Unicode de 16 bits.

```cpp
    #if !defined(_NATIVE_WCHAR_T_DEFINED)
    typedef unsigned short WCHAR;
    #else
    typedef wchar_t WCHAR;
    #endif
```

### <a name="data-types"></a>Tipo de datos

WCHAR

Carácter Unicode de 16 bits.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


