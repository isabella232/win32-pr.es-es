---
description: Un componente con al menos una interfaz queuable es un componente queuable.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Creación de componentes de Queuable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423340"
---
# <a name="creating-queuable-components"></a>Creación de componentes de Queuable

Un componente con al menos una interfaz queuable es un *componente queuable*. Para que una cola invoque un componente, las interfaces se deben marcar como queuable y el componente debe estar instalado en una aplicación en cola. Sin embargo, un componente queuable puede ser un componente de una aplicación no en cola.

Una interfaz queuable debe contener solo parámetros in: sin parámetros de salida y sin valores devueltos. Estas características se comprueban mediante el análisis de la información de tipo durante la instalación del componente. Si la interfaz no es queuable, no se puede activar la cola de la aplicación que contiene el componente.

Para especificar una interfaz de COM+ como queuable, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.

2.  Abra la carpeta **interfaces** del componente de la aplicación com+ que desea convertir en queuable.

3.  Haga clic con el botón secundario en la interfaz que desea marcar como queuable y, a continuación, haga clic en **propiedades**.

4.  Seleccione la pestaña **puesta en cola** en el cuadro de diálogo Propiedades.

5.  Active la casilla de verificación con la etiqueta **en cola**.

    > [!Note]  
    > Si la casilla de verificación **en cola** está atenuada, la interfaz no cumple las restricciones de queuable descritas anteriormente.

     

6.  Haga clic en **OK**.

    Un componente queuable se puede identificar como tal agregando la macro de atributo en cola a la sección interfaz del archivo de código fuente del lenguaje de definición de interfaz (IDL) para todas las interfaces que son queuable.

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear colas de componentes](creating-component-queues.md)
</dt> <dt>

[Desarrollar componentes en cola](developing-queued-components.md)
</dt> </dl>

 

 



