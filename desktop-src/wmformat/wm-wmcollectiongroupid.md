---
title: WM/WMCollectionGroupID
description: El atributo WM/WMCollectionGroupID contiene un GUID que identifica el grupo de recopilación.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- Formato multimedia de Windows WM/WMCollectionGroupID
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b9d89724751e778eb9545b6c743dbfbcf077b860a8d85c5ab9297680deb930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698239"
---
# <a name="wmwmcollectiongroupid"></a>WM/WMCollectionGroupID

El **atributo WM/WMCollectionGroupID** contiene un GUID que identifica el grupo de recopilación.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMCollectionGroupID

## <a name="data-type"></a>Tipo de datos

**GUID DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

El contenido se identifica mediante Windows media mediante tres valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID** y **WM/WMContentID**. Estos valores identifican el contenido, la colección a la que pertenece y el grupo al que pertenece la colección. Los tres valores se rellenan mediante Reproductor de Windows Media cuando se recuperan los metadatos del contenido. Puede hacer que la aplicación registre estos valores y usarlos para identificar el contenido, pero no debe cambiarlos si están presentes.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




