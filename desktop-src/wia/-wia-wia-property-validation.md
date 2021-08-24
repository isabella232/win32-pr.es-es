---
description: Cuando una aplicación realiza una operación IPropertyStorage::WriteMultiple en cualquier propiedad de adquisición de imágenes de Windows (WIA) que se puede escribir, el controlador WIA realiza una validación en el nuevo valor de propiedad.
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Validación de propiedades de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1aca5879dbcb789b7e94a780c8fc99e53b703f6aea74498ae455e8e2ec6b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813055"
---
# <a name="wia-property-validation"></a>Validación de propiedades de WIA

Cuando una aplicación realiza una operación [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) en cualquier propiedad de adquisición de imágenes de Windows (WIA) que se puede escribir, el controlador WIA realiza una validación en el nuevo valor de propiedad. Escribir una propiedad puede tener efectos secundarios que cambien otros valores de propiedad. La aplicación debe leer todos los valores de propiedad después de una operación de escritura para determinar que todas las propiedades están establecidas en valores que la aplicación desea.

Se pueden escribir varias propiedades simultáneamente mediante la [operación IPropertyStorage::WriteMultiple.](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) Puede haber casos en los que algunas asignaciones de propiedades entren en conflicto. En tales casos, la prioridad usada para resolver conflictos es la siguiente:

1.  INTENCIÓN \_ CUR de WIA IPS \_ \_
2.  TIPO DE \_ DATOS IPA DE WIA \_
3.  PROFUNDIDAD \_ DE IPA DE WIA \_
4.  WIA \_ IPS \_ XRES
5.  WIA \_ IPS \_ YRES
6.  WIA \_ IPS \_ XPOS
7.  WIA \_ IPS \_ YPOS
8.  WIA \_ IPS \_ XEXTENT
9.  WIA \_ IPS \_ YEXTENT

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
