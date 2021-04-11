---
description: 'Cuando una aplicación realiza una operación IPropertyStorage:: WriteMultiple en cualquier propiedad de adquisición de imagen de Windows (WIA) grabable, el controlador WIA realiza una validación en el nuevo valor de propiedad.'
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Validación de propiedades de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275446"
---
# <a name="wia-property-validation"></a>Validación de propiedades de WIA

Cuando una aplicación realiza una operación [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) en cualquier propiedad de adquisición de imagen de Windows (WIA) grabable, el controlador WIA realiza una validación en el nuevo valor de propiedad. La escritura de una propiedad puede tener efectos secundarios que cambien otros valores de propiedad. Depende de la aplicación leer todos los valores de propiedad después de una operación de escritura para determinar que todas las propiedades se establecen en los valores que desea la aplicación.

Se pueden escribir varias propiedades simultáneamente mediante la operación [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) . Puede haber casos en los que algunas asignaciones de propiedad estén en conflicto. En estos casos, la prioridad usada para resolver conflictos es la siguiente:

1.  \_intención del \_ CUR de IPS de WIA \_
2.  tipo de DataType del \_ IPA de WIA \_
3.  \_profundidad de IPA de WIA \_
4.  \_XRES de IP WIA \_
5.  \_YRES de IP WIA \_
6.  IP de WIA ( \_ \_ XPOS)
7.  WIA \_ IP \_ YPOS
8.  \_XEXTENT de IP WIA \_
9.  \_YEXTENT de IP WIA \_

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
