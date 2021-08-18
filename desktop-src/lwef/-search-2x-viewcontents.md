---
title: Enumeración ViewContents
description: Usado por el contenido de IResultsViewer para indicar o establecer cómo se muestra el conjunto de retorno de consulta actual.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- ViewContents enumeration Legacy Windows Environment Features
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
ms.openlocfilehash: 2070b68ec62a8dd6ca86758b98a6399ee41180eaad24613d17d0825a927b1871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829115"
---
# <a name="viewcontents-enumeration"></a>Enumeración ViewContents

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

[**IResultsViewer::Contents**](-search-2x-iresultsviewer-contents.md) usa para indicar o establecer cómo se muestra el conjunto de retorno de consulta actual.

## <a name="syntax"></a>Syntax


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

Indica que el tipo de contenido que se muestra en la vista de resultados está establecido actualmente en la vista Shell.

</dd> <dt>

<span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**
</dt> <dd>

Indica que el tipo de contenido que se muestra en la vista de resultados está establecido actualmente en la vista del explorador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>WdsView.idl</dt> </dl> |



 

 





