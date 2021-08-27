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
ms.openlocfilehash: 1eda03d9c08e0e18f1a60e088405919f3982e9de
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476161"
---
# <a name="jet_pcwstr"></a>JET_PCWSTR


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_pcwstr"></a>JET_PCWSTR

El **JET_PCWSTR** tipo de datos contiene una cadena Unicode constante terminada en **NULL** (char \* ).

**Windows Vista: JET_PCWSTR** se presenta en Windows Vista.

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a>Tipo de datos

JET_PCWSTR

Cadena Unicode constante terminada en NULL (char \* ).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


