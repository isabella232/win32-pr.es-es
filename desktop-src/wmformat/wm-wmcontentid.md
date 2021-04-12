---
title: WM/WMContentID
description: El atributo WM/WMContentID contiene un GUID que identifica el contenido.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Formato de Windows Media WM/WMContentID
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419605"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

El atributo **WM/WMContentID** contiene un GUID que identifica el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMContentID

## <a name="data-type"></a>Tipo de datos

**\_GUID de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Las tecnologías de Windows Media identifican el contenido mediante tres valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID** y **WM/WMContentID**. Estos valores identifican el contenido, la colección a la que pertenece y el grupo al que pertenece la colección. Los tres valores se rellenan con Windows Media Player cuando se recuperan los metadatos para el contenido. Puede hacer que la aplicación registre estos valores y utilizarlos para identificar el contenido, pero no debe cambiarlos si están presentes.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




