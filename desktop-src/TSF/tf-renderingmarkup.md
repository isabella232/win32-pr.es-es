---
title: Estructura de TF_RENDERINGMARKUP
description: La estructura de la \_ estructura TF RENDERINGMARKUP contiene un intervalo y la información del atributo display.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- Marco de TF_RENDERINGMARKUP de servicios de texto de estructura
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685624"
---
# <a name="tf_renderingmarkup-structure"></a>\_Estructura RENDERINGMARKUP de TF

La estructura de la estructura [**TF \_ RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) contiene un intervalo y la información del atributo display.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pRange**
</dt> <dd>

Puntero a una interfaz [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) .

</dd> <dt>

**tfDisplayAttr**
</dt> <dd>

Mostrar información de atributos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura no está actualmente en los archivos de encabezado públicos. Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).

 

 




