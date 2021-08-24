---
description: La interfaz IKsPin proporciona un método para recuperar los medios admitidos por un pin en un filtro de modo kernel. IKsPin tiene métodos adicionales además del que se muestra aquí, pero no se admiten para DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interfaz IKsPin (Ksproxy.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 8855378544bcc2ea7357af220b5d80d32edde74a50c304e973c9821aa8e9a41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792335"
---
# <a name="ikspin-interface"></a>Interfaz IKsPin

La `IKsPin` interfaz proporciona un método para recuperar los medios admitidos por un pin en un filtro de modo kernel. `IKsPin`tiene métodos adicionales además del que se muestra aquí, pero no se admiten para DirectShow.

## <a name="members"></a>Miembros

La **interfaz IKsPin** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IKsPin** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IKsPin** tiene estos métodos.



| Método                                          | Descripción                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**KsQueryMediums**](ikspin-ksquerymediums.md) | Recupera los medios admitidos por un pin.<br/> |



 

## <a name="remarks"></a>Comentarios

Debe incluir Ks.h antes de Ksproxy.h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
