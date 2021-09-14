---
description: 'Más información sobre: JET_PCWSTR'
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
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
ms.openlocfilehash: fa07aace787d8fdcc01b5fc4f5ac215f609f9f11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965639"
---
# <a name="jet_pcwstr"></a>JET_PCWSTR


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_pcwstr"></a>JET_PCWSTR

El **JET_PCWSTR** tipo de datos contiene una cadena Unicode constante terminada en **NULL** (char \* ).

**Windows Vista: JET_PCWSTR** se introdujo en Windows Vista.

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a>Tipo de datos

JET_PCWSTR

Cadena Unicode constante terminada en NULL (char \* ).

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


