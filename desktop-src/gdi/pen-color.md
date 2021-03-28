---
description: El atributo color especifica el color del lápiz.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Color del lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d831994ac444207832574dc104a9d5c2582db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544427"
---
# <a name="pen-color"></a>Color del lápiz

El atributo color especifica el color del lápiz. Una aplicación puede crear un lápiz cosmético con un color único mediante la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) para almacenar el tripledo rojo, verde y azul que especifica el color deseado en una estructura [COLORREF](colorref.md) y pasar la dirección de esta estructura a la función [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . (Los lápices de acciones están limitados a negro, blanco e invisible). Para obtener más información sobre los colores y triples RGB, vea [colores](colors.md).

 

 



