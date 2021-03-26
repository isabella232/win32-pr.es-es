---
UID: ''
title: SHIsChildOrSelf función)
description: Compara si una ventana es igual a, un elemento secundario de, o un descendiente de, una segunda ventana.
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
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "104997020"
---
# <a name="shischildorself-function"></a>SHIsChildOrSelf función)

## <a name="description"></a>Descripción

\[Esta función está disponible a través de Windows XP y Windows Server 2003.
Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Compara si una ventana es igual a, un elemento secundario de, o un descendiente de, una segunda ventana.

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a>Parámetros

### <a name="hwndparent-in"></a>hwndParent [in]

Tipo: **hWnd**

Identificador de la primera ventana.

### <a name="hwnd-in"></a>HWND [in]

Tipo: **hWnd**

Identificador de una ventana que se va a probar con *hwndParent*.

## <a name="returns"></a>Devoluciones

Tipo: **HRESULT**

Devuelve **S_OK** si la ventana especificada por *hWnd* es igual a, un elemento secundario de o un descendiente de la ventana especificada por *hwndParent*.
Devuelve **S_FALSE** si la ventana especificada por HWND no es igual a, no es un elemento secundario de, y no es un descendiente de la ventana especificada por *hwndParent*.
El valor devuelto es indefinido si alguno de los identificadores de ventana no es válido.

## <a name="remarks"></a>Observaciones

## <a name="see-also"></a>Vea también

[Ischild (](/windows/desktop/api/winuser/nf-winuser-ischild)
