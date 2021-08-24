---
description: Un componente con al menos una interfaz que se puede cola es un componente que se puede usar.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Creación de componentes que se pueden crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ca7b4717da44145121508ed3e8b208e8401a240f1a2ceb858be299bf2b32f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637845"
---
# <a name="creating-queuable-components"></a>Creación de componentes que se pueden crear

Un componente con al menos una interfaz que se puede cola es *un componente que se puede usar.* Para que una cola invoque un componente, las interfaces deben marcarse como queuable y el componente debe instalarse en una aplicación en cola. Sin embargo, un componente que se puede poner en cola puede ser un componente de una aplicación no en cola.

Una interfaz que se puede cola solo debe contener en parámetros, sin parámetros out ni valores devueltos. Estas características se comprueban mediante el análisis de la información de tipo durante la instalación del componente. Si la interfaz no se puede poner en cola, no se puede activar la cola de la aplicación que contiene el componente.

Para especificar una interfaz COM+ como queuable, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en Servicios de componentes **,** abra la carpeta **Aplicaciones COM+** asociada al equipo que desea administrar.

2.  Abra la **carpeta Interfaces** del componente de la aplicación COM+ que desea hacer que se puedan hacer colas.

3.  Haga clic con el botón derecho en la interfaz que desea marcar como queuable y, a continuación, haga clic en **Propiedades.**

4.  Seleccione la **pestaña Cola en** el cuadro de diálogo de propiedades.

5.  Active la casilla con la etiqueta **Queued**.

    > [!Note]  
    > Si la **casilla En** cola está atenuada, la interfaz no satisface las restricciones que se pueden poner en cola descritas anteriormente.

     

6.  Haga clic en **Aceptar**.

    Un componente que se puede identificar como tal agregando la macro de atributo QUEUEABLE a la sección Interfaz del archivo de origen del Lenguaje de definición de interfaz (IDL) para todas las interfaces que se pueden poner en cola.

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

[Desarrollo de componentes en cola](developing-queued-components.md)
</dt> </dl>

 

 



