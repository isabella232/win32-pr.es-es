---
description: Las dimensiones de un lápiz torético se especifican en unidades de dispositivo.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Lápices lápices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474340"
---
# <a name="cosmetic-pens"></a>Lápices lápices

Las dimensiones de un lápiz torético se especifican en unidades de dispositivo. Por lo tanto, las líneas dibujadas con un lápiz tortil siempre tienen un ancho fijo. Por lo general, las líneas dibujadas con un lápiz de geometría se dibujan de 3 a 10 veces más rápido que las líneas dibujadas con un lápiz geométrico. Los lápices de color tienen tres atributos: ancho, estilo y color. Para obtener más información sobre estos atributos, vea [Pen Attributes](pen-attributes.md).

Para crear un lápiz, use la [**función CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) Para recuperar uno de los tres lápices de acción que administra el sistema, use la [**función GetStockObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)

Después de crear un lápiz (u obtener un identificador para uno de los lápices estándar), seleccione el lápiz en el contexto de dispositivo (DC) de la aplicación mediante la [**función SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) A partir de este punto, la aplicación usa este lápiz para cualquier operación de dibujo de línea en su área cliente.

 

 



