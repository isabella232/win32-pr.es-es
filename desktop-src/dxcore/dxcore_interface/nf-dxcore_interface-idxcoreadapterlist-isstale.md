---
title: IDXCoreAdapterList::IsStale
description: Determina si los cambios en este sistema han dado lugar a que este objeto de lista de adaptadores DXCore se haya quedarse sin fecha.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a40a590a76773592d5442993c75149b2349880f7681d625e777d363062f5c4be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502576"
---
# <a name="idxcoreadapterlistisstale-method"></a>IDXCoreAdapterList::IsStale (método)

Determina si los cambios en este sistema han dado lugar a que este objeto de lista de adaptadores DXCore se haya quedarse sin fecha. Para obtener instrucciones de programación y ejemplos de código, vea [Uso de DXCore para enumerar adaptadores.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve si, desde que se genera la lista, se han producido cambios en las condiciones del sistema que harían que esta lista de `true` adaptadores quedara obsoleta. De lo contrario, devuelve `false`.

## <a name="remarks"></a>Comentarios

Puede sondear **IsStale para** determinar si los cambios en las condiciones del sistema han provocado que esta lista esté obsoleta. Si **IsStale devuelve** una vez, devuelve durante la duración restante del objeto de lista `true` de `true` adaptadores DXCore. Un objeto de lista obsoleto todavía se considera obsoleto aunque las condiciones del sistema vuelvan a un estado que coincida con la lista (las mismas condiciones se obtienen ahora que cuando se generó la lista por primera vez).

## <a name="see-also"></a>Consulte también

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Referencia de DXCore](../dxcore-reference.md), [Uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)