---
title: El estado de la canalización
description: En el servidor, el compilador MIDL crea una variable de estado que coordina los procedimientos de inserción, extracción y asignación.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149426"
---
# <a name="the-pipe-state"></a>El estado de la canalización

En el servidor, el compilador MIDL crea una variable de *Estado* que coordina los procedimientos de inserción, extracción y asignación. En el lado del cliente, el desarrollador debe crear la variable de *Estado* . Por lo tanto, la variable de *Estado* es local en ambos lados, es decir, cada cliente y servidor mantienen su propio estado de canalización. El código auxiliar del servidor mantiene la variable de estado en el servidor. No debe intentar modificar su contenido directamente. El cliente debe inicializar los campos de la estructura de control de canalización y mantener su variable de *Estado* . Utiliza la variable de *Estado* para identificar dónde ubicar o colocar los datos.

La variable de *Estado* de cliente puede ser tan simple como un identificador de archivo, si va a transferir datos de un archivo a otro. También puede ser un entero que apunte a un elemento de una matriz. O bien, puede definir una estructura de estado bastante compleja para realizar tareas adicionales, como coordinar las rutinas de inserción y extracción en un \[ parámetro [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] .

 

 