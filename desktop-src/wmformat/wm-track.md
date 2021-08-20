---
title: WM/Track
description: El atributo WM/Track contiene el número de pista del contenido. Este atributo está basado en cero y se admite por compatibilidad con versiones anteriores. El nuevo contenido debe usar el atributo WM/TrackNumber en su lugar.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- Formato multimedia de Windows WM/Track
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1113fde7b0b29b6f1f7618e9d531df83070725b9e05e70e09f64f93b027abfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026943"
---
# <a name="wmtrack"></a>WM/Track

El **atributo WM/Track** contiene el número de pista del contenido. Este atributo está basado en cero y se admite por compatibilidad con versiones anteriores. El nuevo contenido debe usar el [**atributo WM/TrackNumber**](wm-tracknumber.md) en su lugar.

## <a name="global-constant"></a>Constante global

g \_ wszWMTrack

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Comentarios

Muchas aplicaciones existentes escriben el valor **de WM/Track** como **DWORD.** Si crea una aplicación que reproduce archivos de orígenes desconocidos, debe incluir código para controlar los valores de cadena y **DWORD.**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




