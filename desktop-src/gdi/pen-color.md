---
description: El atributo de color especifica el color del lápiz.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Color del lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e88d73fc80f6fe02a6d9e1de1d33568c94e05768f113c8bee0754c5d8afb418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886210"
---
# <a name="pen-color"></a>Color del lápiz

El atributo de color especifica el color del lápiz. Una aplicación puede crear un lápiz con un color único usando la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) para almacenar el triplete rojo, verde y azul que especifica el color deseado en una estructura [COLORREF](colorref.md) y pasando la dirección de esta estructura a la función [**CreatePen,**](/windows/desktop/api/Wingdi/nf-wingdi-createpen) [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) (Los lápices de existencias se limitan a negro, blanco e invisible). Para obtener más información sobre los tripletes RGB y el color, vea [Colores.](colors.md)

 

 



