---
title: Enumeración PreviewDisplayStyle
description: Lo utiliza IResultsViewer PreviewStyle para establecer o determinar el estilo de presentación que se está usando actualmente.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- Enumeración PreviewDisplayStyle características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- PreviewDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11902821ec9fdbbaa9ab8d3fda8971f42fc28c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700274"
---
# <a name="previewdisplaystyle-enumeration"></a>Enumeración PreviewDisplayStyle

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Usado por [**IResultsViewer::P reviewstyle**](-search-2x-iresultsviewer-previewstyle.md) para establecer o determinar el estilo de presentación que se está usando actualmente.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**Vista previa automática**
</dt> <dd>

Indica la vista previa automática.

</dd> <dt>

<span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**
</dt> <dd>

Indica RightPreview.

</dd> <dt>

<span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**
</dt> <dd>

Indica BottomPreview.

</dd> <dt>

<span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**Novista previa**
</dt> <dd>

Indica Preview.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





