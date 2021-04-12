---
title: Bookmark (evento)
description: Bookmark (evento)
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268613"
---
# <a name="bookmark-event"></a>Bookmark (evento)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando se activa un marcador en una cadena de texto de voz que ha definido la aplicación.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

Marcador de **Sub** *Agent* \_  **(ByVal** *BookmarkID ** * *)*



| Parte         | Descripción                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Entero largo que identifica el número de marcador. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Para especificar un evento de marcador, use el método [**Speak**](speak-method.md) con una etiqueta **MRK** en el texto proporcionado. Para obtener más información acerca de las etiquetas, consulte etiquetas de salida de voz.

 

 




