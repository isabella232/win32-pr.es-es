---
title: Bookmark (Evento)
description: Bookmark (Evento)
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6a6dcd072b87c6a924c8d33e6ebb73c75c927bdf955f51612703d3fc18af79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976715"
---
# <a name="bookmark-event"></a>Bookmark (Evento)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando se activa un marcador en una cadena de texto de voz definida por la aplicación.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Marcador** *del* sub \_ **agente** **(ByVal** *BookmarkID))**



| Parte         | Descripción                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Entero Long que identifica el número de marcador. |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

Para especificar un evento de marcador, use el [**método Speak**](speak-method.md) con una **etiqueta Mrk** en el texto proporcionado. Para más información sobre las etiquetas, consulte Etiquetas de salida de voz.

 

 




