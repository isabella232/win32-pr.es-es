---
title: WM/WMCollectionID
description: El atributo WM/WMCollectionID contiene un GUID que identifica la colección.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- Formato multimedia de windows WM/WMCollectionID
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ad7e22c6769d459dc3d99b964a2df8e4dc562c709a231163d05a1b6b0be911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928835"
---
# <a name="wmwmcollectionid"></a>WM/WMCollectionID

El **atributo WM/WMCollectionID** contiene un GUID que identifica la colección.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMCollectionID

## <a name="data-type"></a>Tipo de datos

**GUID DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

El contenido se identifica mediante Windows Media mediante tres valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID y** **WM/WMContentID**. Estos valores identifican el contenido, la colección a la que pertenece y el grupo al que pertenece la colección. Los tres valores se rellenan mediante Reproductor de Windows Media cuando se recuperan los metadatos del contenido. Puede hacer que la aplicación registre estos valores y usarlos para identificar el contenido, pero no debe cambiarlos si están presentes.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




