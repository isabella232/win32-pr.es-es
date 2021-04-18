---
title: Enumeración ViewContents
description: Utilizado por el contenido de IResultsViewer para indicar o establecer cómo se muestra el conjunto de devoluciones de la consulta actual.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- Enumeración ViewContents características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700372"
---
# <a name="viewcontents-enumeration"></a>Enumeración ViewContents

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Usado por [**IResultsViewer:: Contents**](-search-2x-iresultsviewer-contents.md) para indicar o establecer cómo se muestra el conjunto de devoluciones de la consulta actual.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**
</dt> <dd>

Indica el tipo de contenido que se muestra en la vista de resultados.

</dd> <dt>

<span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**
</dt> <dd>

Indica que el tipo de contenido que se muestra en la vista de resultados está establecido actualmente en la vista de Shell.

</dd> <dt>

<span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**
</dt> <dd>

Indica que el tipo de contenido que se muestra en la vista de resultados está establecido actualmente en la vista de explorador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





