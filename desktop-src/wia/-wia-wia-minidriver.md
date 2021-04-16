---
description: Las aplicaciones ven los dispositivos de adquisición de imágenes de Windows (WIA) como un árbol jerárquico de objetos IWiaItem o IWiaItem2 con el elemento raíz que representa el propio dispositivo.
ms.assetid: ae4ded93-09be-4caa-ad6e-1a9071fdb4b6
title: Minicontrolador WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aadaf55cfe2e8102d4e0e02cf9787b9696e327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541907"
---
# <a name="wia-minidriver"></a>Minicontrolador WIA

Las aplicaciones ven los dispositivos de adquisición de imágenes de Windows (WIA) como un árbol jerárquico de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) con el elemento raíz que representa el propio dispositivo. Los dispositivos WIA se pueden usar simultáneamente en más de una aplicación. Por lo tanto, es necesario que la vista de cada aplicación de un objeto **IWiaItem** o **IWiaItem2** sea independiente de las vistas de otra aplicación. Esto se logra con dos objetos de elemento diferentes. El controlador crea el árbol de elementos de controlador de los objetos de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , también denominados elementos de controlador, mediante los métodos de los servicios del controlador WIA. Son objetos globales que el controlador usa para representar los elementos internos de cada controlador. Cuando una aplicación crea un objeto **IWiaItem** o **IWiaItem2** (también denominado elemento de aplicación), este objeto está vinculado a la [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondiente del controlador en el árbol de elementos de controlador. Un recuento de referencias se mantiene en el objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) sujeto a las siguientes reglas:

-   Cuando un controlador agrega un objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) al árbol de elementos de controlador, se incrementa el recuento de referencias del objeto de la [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) . Esto suele producirse durante [IWiaMiniDrv::D rvinitializewia](https://msdn.microsoft.com/library/ms794097.aspx) o cuando \_ \_ se procesa un comando WIA cmd SYNCHRONIZE.
-   Cuando un controlador quita un objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) del árbol de elementos de controlador, se reduce el recuento de referencias del objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) y el objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) se marca para que no pueda tener acceso al dispositivo de nuevo. Normalmente, esto se produce cuando se desconecta un dispositivo o se elimina un elemento. Las aplicaciones todavía pueden leer las propiedades de un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) incluso cuando se ha quitado el objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondiente del árbol de elementos de controlador.
-   Cuando se crea un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) , se vincula a un objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondiente. Se incrementa el recuento de referencias del objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) .
-   Cuando se libera un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) , se rompe el vínculo al objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) correspondiente y se reduce el recuento de referencias del objeto de la [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) .
-   Si el recuento de referencias de un objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) va a cero, se elimina el objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) . Esto se aplica a todos los objetos de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , incluido el elemento raíz. El recuento de referencias de un objeto de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) solo llega a cero cuando ningún elemento de aplicación hace referencia a él y ya no está vinculado al árbol de elementos de controlador.

Con este esquema de recuento de referencias, muchos objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) se pueden vincular a una [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) sin interferencias. Dado que cada **IWiaItem** o **IWiaItem2** contiene su propio almacenamiento de propiedades, una aplicación puede continuar leyendo las propiedades del elemento incluso después de que se haya eliminado un elemento, pero no se realizará correctamente ninguna operación que requiera el acceso al dispositivo. Dado que las propiedades de los elementos se almacenan en el objeto **IWiaItem** o **IWiaItem2** , el controlador debe establecer las propiedades del objeto **IWiaItem** o **IWiaItem2** en el dispositivo antes de una transferencia de datos.

 

 



