---
title: TF_RENDERINGMARKUP estructura
description: La estructura \_ TF RENDERINGMARKUP contiene un intervalo y la información del atributo para mostrar.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- TF_RENDERINGMARKUP estructura Text Services Framework
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d594ae41109e072413e20709c68770038fbae870966325f762ddd169900491d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118874210"
---
# <a name="tf_renderingmarkup-structure"></a>Estructura \_ DE TF RENDERINGMARKUP

La [**estructura \_ TF RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) contiene un intervalo y la información del atributo para mostrar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Prange**
</dt> <dd>

Puntero a una [interfaz ITfRange.](/windows/desktop/api/Msctf/nn-msctf-itfrange)

</dd> <dt>

**tfDisplayAttr**
</dt> <dd>

Mostrar información de atributos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura no está actualmente en los archivos de encabezado público. Para usar esta API, debe compilar midl el [prototipo](prototypes.md).

 

 




