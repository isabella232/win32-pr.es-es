---
title: WM/WMContentID
description: El atributo WM/WMContentID contiene un GUID que identifica el contenido.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Formato multimedia de Windows WM/WMContentID
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6b1b77bf0305fa0890ea7e85172d77d6e213864c1fc114136bc42e08a8507b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083869"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

El **atributo WM/WMContentID** contiene un GUID que identifica el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMContentID

## <a name="data-type"></a>Tipo de datos

**GUID DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

El contenido se identifica mediante Windows media mediante tres valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID** y **WM/WMContentID**. Estos valores identifican el contenido, la colección a la que pertenece y el grupo al que pertenece la colección. Los tres valores se rellenan mediante Reproductor de Windows Media cuando se recuperan los metadatos del contenido. Puede hacer que la aplicación registre estos valores y usarlos para identificar el contenido, pero no debe cambiarlos si están presentes.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




