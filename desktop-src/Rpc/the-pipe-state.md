---
title: Estado de canalización
description: En el servidor, el compilador MIDL crea una variable de estado que coordina los procedimientos de inserción, extracción y asignación.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d12c5ef5549d89f3aee2833599f5930f2617478e66e16c3b78188eb63a40e7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924075"
---
# <a name="the-pipe-state"></a>Estado de canalización

En el servidor, el compilador MIDL crea una variable *de* estado que coordina los procedimientos de inserción, extracción y asignación. En el lado cliente, el desarrollador debe crear la variable *de* estado. Por lo tanto, *la* variable de estado es local para ambos lados, es decir, el cliente y el servidor mantienen su propio estado de canalización. El código auxiliar del servidor mantiene la variable de estado en el servidor. No debe intentar modificar su contenido directamente. El cliente debe inicializar los campos en la estructura de control de canalización y mantener su variable *de* estado. Usa la variable *de estado* para identificar dónde buscar o colocar los datos.

La variable *de estado* de cliente puede ser tan simple como un identificador de archivo, si va a transferir datos de un archivo a otro. También puede ser un entero que apunta a un elemento de una matriz. O bien, puede definir una estructura de estado bastante compleja para realizar tareas adicionales, como coordinar las rutinas de inserción y extracción en un parámetro de entrada \[ [](/windows/desktop/Midl/in) [y](/windows/desktop/Midl/out-idl) \] salida.

 

 