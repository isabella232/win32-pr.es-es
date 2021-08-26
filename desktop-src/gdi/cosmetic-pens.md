---
description: Las dimensiones de un lápiz torético se especifican en unidades de dispositivo.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Lápices lápices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65f875ce5873b5f53cba19b5440751b8ac7683df99765ea7e8e6eec813ef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966075"
---
# <a name="cosmetic-pens"></a>Lápices lápices

Las dimensiones de un lápiz torético se especifican en unidades de dispositivo. Por lo tanto, las líneas dibujadas con un lápiz tortil siempre tienen un ancho fijo. Por lo general, las líneas dibujadas con un lápiz de geometría se dibujan de 3 a 10 veces más rápido que las líneas dibujadas con un lápiz geométrico. Los lápices de color tienen tres atributos: ancho, estilo y color. Para obtener más información sobre estos atributos, vea [Pen Attributes](pen-attributes.md).

Para crear un lápiz, use la [**función CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) Para recuperar uno de los tres lápices de acción que administra el sistema, use la [**función GetStockObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)

Después de crear un lápiz (u obtener un identificador para uno de los lápices estándar), seleccione el lápiz en el contexto de dispositivo (DC) de la aplicación mediante la [**función SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) A partir de este punto, la aplicación usa este lápiz para cualquier operación de dibujo de línea en su área cliente.

 

 



