---
UID: ''
title: Función SHIsChildOrSelf
description: Compara si una ventana es igual a, un elemento secundario de o un descendiente de, una segunda ventana.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: f2d8eaab0f17647a6f548a0243199073baef074c88dad6a3f7100cfbca1a02be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941335"
---
# <a name="shischildorself-function"></a>Función SHIsChildOrSelf

## <a name="description"></a>Descripción

\[Esta función está disponible a través Windows XP y Windows Server 2003.
Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Compara si una ventana es igual a, un elemento secundario de o un descendiente de, una segunda ventana.

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a>Parámetros

### <a name="hwndparent-in"></a>hwndParent [in]

Tipo: **HWND**

Identificador de la primera ventana.

### <a name="hwnd-in"></a>hwnd [in]

Tipo: **HWND**

Identificador de una ventana que se va a probar *con hwndParent*.

## <a name="returns"></a>Devoluciones

Tipo: **HRESULT**

Devuelve **S_OK** si la ventana especificada por *hwnd* es igual a, un elemento secundario de o un descendiente de la ventana especificada por *hwndParent*.
Devuelve **S_FALSE** si la ventana especificada por hwnd no es igual a, no es un elemento secundario de y no es un descendiente de la ventana especificada por *hwndParent*.
El valor devuelto no está definido si alguno de los identificadores de ventana no es válido.

## <a name="remarks"></a>Comentarios

## <a name="see-also"></a>Vea también

[IsChild](/windows/desktop/api/winuser/nf-winuser-ischild)
