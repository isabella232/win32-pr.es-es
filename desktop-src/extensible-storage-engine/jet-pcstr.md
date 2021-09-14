---
description: 'Más información sobre: JET_PCSTR'
title: JET_PCSTR
TOCTitle: JET_PCSTR
ms:assetid: 5826e6b9-5297-421f-abaa-016708bf16f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269254(v=EXCHG.10)
ms:contentKeyID: 32765556
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
ms.openlocfilehash: 6a698afffb415bb4418f46cfe16091ceda03cb59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965640"
---
# <a name="jet_pcstr"></a>JET_PCSTR


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_pcstr"></a>JET_PCSTR

El **JET_PCSTR** tipo de datos contiene una cadena ASCII constante terminada en **NULL** (char \* ).

**Windows Vista: JET_PCSTR** se introdujo en Windows Vista.

```cpp
    typedef __nullterminated const char *  JET_PCSTR;
```

### <a name="data-types"></a>Tipo de datos

JET_PCSTR

Cadena ASCII constante terminada en NULL (char \* ).

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


