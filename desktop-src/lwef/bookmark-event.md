---
title: Bookmark (Evento)
description: Bookmark (Evento)
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072394"
---
# <a name="bookmark-event"></a>Bookmark (Evento)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando se activa un marcador en una cadena de texto de voz definida por la aplicación.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Marcador** *del* sub \_ **agente** **(ByVal** *BookmarkID...))**



| Parte         | Descripción                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Entero Long que identifica el número de marcador. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Para especificar un evento de marcador, use el [**método Speak**](speak-method.md) con una **etiqueta Mrk** en el texto proporcionado. Para más información sobre las etiquetas, consulte Etiquetas de salida de voz.

 

 




