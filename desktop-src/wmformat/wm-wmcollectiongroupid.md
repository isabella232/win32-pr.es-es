---
title: WM/WMCollectionGroupID
description: El atributo WM/WMCollectionGroupID contiene un GUID que identifica el grupo de recopilación.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- Formato de Windows Media WM/WMCollectionGroupID
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652007933669db4ed7977474858c7089ca0d577f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419606"
---
# <a name="wmwmcollectiongroupid"></a>WM/WMCollectionGroupID

El atributo **WM/WMCollectionGroupID** contiene un GUID que identifica el grupo de recopilación.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMCollectionGroupID

## <a name="data-type"></a>Tipo de datos

**\_GUID de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Las tecnologías de Windows Media identifican el contenido mediante tres valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID** y **WM/WMContentID**. Estos valores identifican el contenido, la colección a la que pertenece y el grupo al que pertenece la colección. Los tres valores se rellenan con Windows Media Player cuando se recuperan los metadatos para el contenido. Puede hacer que la aplicación registre estos valores y utilizarlos para identificar el contenido, pero no debe cambiarlos si están presentes.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




