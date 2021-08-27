---
description: Las aplicaciones Windows dispositivos de adquisición de imágenes (WIA) como un árbol jerárquico de objetos IWiaItem o IWiaItem2 con el elemento raíz que representa el propio dispositivo.
ms.assetid: ae4ded93-09be-4caa-ad6e-1a9071fdb4b6
title: WIA Minidriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e8d3c520106c345bd02df5b686bb1abf34f9ff1aa0b338e645b178cabbb874
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056925"
---
# <a name="wia-minidriver"></a>WIA Minidriver

Las aplicaciones Windows dispositivos de adquisición de imágenes (WIA) como un árbol jerárquico de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) con el elemento raíz que representa el propio dispositivo. Más de una aplicación puede usar dispositivos WIA simultáneamente. Por lo tanto, es necesario que la vista de cada aplicación de un **objeto IWiaItem** o **IWiaItem2** sea independiente de las vistas de otra aplicación. Esto se logra al tener dos objetos de elemento diferentes. El controlador crea el árbol de elementos de controlador de objetos [IWiaDrvItem Interface,](https://msdn.microsoft.com/library/ms793976.aspx) también denominados elementos de controlador, mediante los métodos de servicios de controlador WIA. Se trata de objetos globales que el controlador usa para representar los elementos internos de cada controlador. Cuando una aplicación crea un objeto **IWiaItem** o **IWiaItem2** (también denominado elemento de aplicación), este objeto se vincula a la interfaz [IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondiente del controlador en el árbol de elementos del controlador. Se mantiene un recuento de referencias en el objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) sujeto a las reglas siguientes:

-   Cuando un controlador agrega un objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) al árbol de elementos del controlador, se incrementa el recuento de referencias del objeto [IWiaDrvItem Interface.](https://msdn.microsoft.com/library/ms793976.aspx) Esto suele ocurrir durante [IWiaMiniDrv::d rvInitializeWia](https://msdn.microsoft.com/library/ms794097.aspx) o cuando se procesa un comando \_ CMD SYNCHRONIZE de WIA. \_
-   Cuando un controlador quita un objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) del árbol de elementos del controlador, se disminuye el recuento de referencias del objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) y el objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) se marca para que no pueda volver a acceder al dispositivo. Esto suele ocurrir cuando se desconecta un dispositivo o se elimina un elemento. Las aplicaciones todavía pueden leer propiedades de un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) incluso cuando el objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) correspondiente se ha quitado del árbol de elementos del controlador.
-   Cuando se crea un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2,**](-wia-iwiaitem2.md) se vincula a un objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) correspondiente. Se incrementa el recuento de referencias del objeto [IWiaDrvItem Interface.](https://msdn.microsoft.com/library/ms793976.aspx)
-   Cuando se libera un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2,**](-wia-iwiaitem2.md) se grave el vínculo a su objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) correspondiente y se disminuye el recuento de referencias del objeto [IWiaDrvItem Interface.](https://msdn.microsoft.com/library/ms793976.aspx)
-   Si el recuento de referencias de un objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) va a cero, se elimina el objeto [IWiaDrvItem Interface.](https://msdn.microsoft.com/library/ms793976.aspx) Esto se aplica a todos los [objetos IWiaDrvItem Interface,](https://msdn.microsoft.com/library/ms793976.aspx) incluido el elemento raíz. El recuento de referencias de un objeto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) solo va a cero cuando ningún elemento de aplicación hace referencia a él y ya no está vinculado al árbol de elementos del controlador.

Con este esquema de recuento de referencias, muchos objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) pueden vincularse a una interfaz [IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) sin interferencias. Dado que **cada IWiaItem** o **IWiaItem2** contiene su propio almacenamiento de propiedades, una aplicación puede seguir leyendo las propiedades del elemento incluso después de eliminar un elemento, pero ninguna operación que requiera acceso al dispositivo se realizará correctamente. Dado que las propiedades de elemento se almacenan en el objeto **IWiaItem** o **IWiaItem2,** el controlador debe establecer las propiedades del objeto **IWiaItem** o **IWiaItem2** en el dispositivo antes de una transferencia de datos.

 

 



