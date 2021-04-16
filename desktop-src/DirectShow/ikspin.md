---
description: La interfaz IKsPin proporciona un método para recuperar los medios admitidos por un PIN en un filtro de modo kernel. IKsPin tiene métodos adicionales además del que se muestra aquí, pero no se admiten para DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interfaz IKsPin (ksproxy. h)
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
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677116"
---
# <a name="ikspin-interface"></a>Interfaz IKsPin

La `IKsPin` interfaz proporciona un método para recuperar los medios admitidos por un PIN en un filtro de modo kernel. `IKsPin` tiene métodos adicionales además del que se muestra aquí, pero no se admiten para DirectShow.

## <a name="members"></a>Miembros

La interfaz **IKsPin** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IKsPin** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IKsPin** tiene estos métodos.



| Método                                          | Descripción                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**KsQueryMediums**](ikspin-ksquerymediums.md) | Recupera los medios admitidos por un PIN.<br/> |



 

## <a name="remarks"></a>Observaciones

Debe incluir KS. h antes de ksproxy. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
