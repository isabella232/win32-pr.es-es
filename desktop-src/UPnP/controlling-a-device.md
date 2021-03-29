---
title: Controlar un dispositivo
description: Una vez que haya detectado dispositivos, puede controlarlos.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff91339c67b67de5d3e90eda0ce64ebcc68b9e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903794"
---
# <a name="controlling-a-device"></a>Controlar un dispositivo

Una vez que haya detectado dispositivos, puede controlarlos.

**Para ver las propiedades del dispositivo**

1.  Seleccione un dispositivo en la lista **dispositivos encontrados** .
2.  Haga clic en **propiedades del dispositivo**. La ventana **propiedades del dispositivo** aparece con la información solicitada.

> [!Note]  
> La funcionalidad de presentación de la **vista** no está disponible en el código de ejemplo de C++.

 

**Para ver la página de presentación de un dispositivo**

1.  Seleccione un dispositivo en la lista **dispositivos encontrados** .
2.  Haga clic en **ver presentación**. Aparece una ventana de Internet Explorer con la página de presentación solicitada.

> [!Note]  
> La funcionalidad de **ver Descripción de servicio** no está disponible en el código de ejemplo de C++.

 

**Para ver una descripción del servicio**

1.  Puede escribir la dirección URL de la descripción del servicio en la descripción del **servicio. Campo de dirección URL** .

    ![URL de descripción de servicio](images/ucp-url.png)

2.  Haga clic en **ver Descripción del servicio.** Se muestra la ventana **visor de descripción de servicio** . A continuación, puede examinar la descripción del servicio mediante la vista de árbol. Esta funcionalidad no está disponible en el código de ejemplo de C++.

    ![ventana del visor de descripción de servicio](images/ucp-serv.png)

    Hay cinco comandos que puede usar en la ventana del visor de descripción de servicio.



| Botón                 | Acción realizada                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Go                     | Carga el archivo que se muestra en la **Descripción del servicio. Campo de dirección URL** .                                                                                                                              |
| Establecer acción             | Seleccione un nombre de acción en el árbol de Descripción del servicio y haga clic en **establecer acción**. El nombre de la acción se escribe en el campo **invocar acción** de la ventana principal del **UCP** .       |
| Establecer variable           | Seleccione un nombre de variable en el árbol de Descripción del servicio y haga clic en **establecer variable**. El nombre de la variable se escribe en el campo **variable de consulta** de la ventana principal del **UCP** . |
| Rellenar lista de variables | Carga todos los nombres de variable del servicio en la lista de **variables de consulta** de la ventana principal del **UCP** .                                                                           |
| Rellenar lista de acciones   | Carga todos los nombres de acción del servicio en la lista de **acciones de invocación** de la ventana principal del **UCP** .                                                                              |



 

**Para controlar un dispositivo**

1.  En la lista **dispositivos encontrados** , seleccione el dispositivo que desea controlar.
2.  En la lista **elegir servicio** , seleccione el servicio que desea invocar o la variable de estado que desea consultar.

    ![ventana controlar dispositivos](images/ucp-contr.png)

    > [!Note]  
    > El contenido de la **lista de servicios** se basa en el dispositivo seleccionado en la lista **dispositivos encontrados** .

     

3.  Si desea averiguar el valor de una variable de estado para el servicio seleccionado, escriba el nombre de la variable en el campo **variable de consulta** para servicio. Haga clic en **Consulta**. Los resultados se muestran en el campo **valor de estado de consulta/argumentos de acción de salida** .
4.  Si desea invocar una acción para un servicio, escriba el nombre de la acción en el campo **invocar acción** y los argumentos en el campo argumentos de la **acción** . Haga clic en **invocar**. Los resultados se muestran en el campo **valor de estado de consulta/argumentos de acción out** , si los hay.

    El valor devuelto, si existe, está incluido en el primer argumento out.

    > [!Note]  
    > Si hay varios argumentos para una acción, sepárelos con espacios.

     

5.  Ver información de eventos en el campo **eventos** del servicio seleccionado.

 

 




