---
title: WM/pista
description: El atributo WM/Track contiene el número de pista del contenido. Este atributo es de base cero y se admite por compatibilidad con versiones anteriores. En su lugar, el nuevo contenido debe usar el atributo WM/TrackNumber.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- Formato de Windows Media de WM/seguimiento
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419293"
---
# <a name="wmtrack"></a>WM/pista

El atributo **WM/Track** contiene el número de pista del contenido. Este atributo es de base cero y se admite por compatibilidad con versiones anteriores. En su lugar, el nuevo contenido debe usar el atributo [**WM/TrackNumber**](wm-tracknumber.md) .

## <a name="global-constant"></a>Constante global

g \_ wszWMTrack

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Muchas aplicaciones existentes escriben el valor de **WM/Track** como **DWORD**. Si crea una aplicación que reproduzca archivos de orígenes desconocidos, debe incluir código para controlar los valores de cadena y **DWORD** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




