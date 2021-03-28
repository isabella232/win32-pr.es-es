---
description: Las dimensiones de un lápiz cosmético se especifican en unidades de dispositivo.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Bolígrafos cosméticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812001"
---
# <a name="cosmetic-pens"></a>Bolígrafos cosméticas

Las dimensiones de un lápiz cosmético se especifican en unidades de dispositivo. Por lo tanto, las líneas dibujadas con un lápiz cosmético siempre tienen un ancho fijo. Las líneas dibujadas con un lápiz cosmético generalmente se dibujan de 3 a 10 veces más rápido que las líneas dibujadas con un lápiz geométrico. Los lápices estéticos tienen tres atributos: ancho, estilo y color. Para obtener más información sobre estos atributos, vea [Pen Attributes](pen-attributes.md).

Para crear un lápiz cosmético, use la función [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Para recuperar una de las tres plumillas cosméticas de acciones administradas por el sistema, use la función [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) .

Después de crear un lápiz (u obtener un identificador a uno de los lápices de bolsa), seleccione el lápiz en el contexto de dispositivo (DC) de la aplicación mediante la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . A partir de este punto, la aplicación usa este lápiz para todas las operaciones de dibujo de líneas en su área de cliente.

 

 



