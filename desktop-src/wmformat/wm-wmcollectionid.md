---
title: WM/WMCollectionID
description: El atributo WM/WMCollectionID contiene un GUID que identifica la colección.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- Formato de Windows Media WM/WMCollectionID
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d2ffe9ca827b19b4ce403b2e2929dea64ae684
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419607"
---
# <a name="wmwmcollectionid"></a>WM/WMCollectionID

El atributo **WM/WMCollectionID** contiene un GUID que identifica la colección.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMCollectionID

## <a name="data-type"></a>Tipo de datos

**\_GUID de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Las tecnologías de Windows Media identifican el contenido mediante tres valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID** y **WM/WMContentID**. Estos valores identifican el contenido, la colección a la que pertenece y el grupo al que pertenece la colección. Los tres valores se rellenan con Windows Media Player cuando se recuperan los metadatos para el contenido. Puede hacer que la aplicación registre estos valores y utilizarlos para identificar el contenido, pero no debe cambiarlos si están presentes.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




