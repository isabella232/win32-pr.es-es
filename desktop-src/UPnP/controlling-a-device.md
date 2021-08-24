---
title: Controlar un dispositivo
description: Una vez que haya detectado dispositivos, puede controlarlos.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79d6e6993794a4af972af8538b9b1cd56902c34596197836990028b2761ffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656080"
---
# <a name="controlling-a-device"></a>Controlar un dispositivo

Una vez que haya detectado dispositivos, puede controlarlos.

**Para ver las propiedades del dispositivo**

1.  Seleccione un dispositivo en la lista **Dispositivos encontrados.**
2.  Haga clic **en Propiedades del dispositivo**. Aparece **la ventana Propiedades** del dispositivo con la información solicitada.

> [!Note]  
> La **funcionalidad Ver presentación** no está disponible en el código de ejemplo de C++.

 

**Para ver la página de presentación de un dispositivo**

1.  Seleccione un dispositivo en la lista **Dispositivos encontrados.**
2.  Haga clic **en Ver presentación.** Aparece Internet Explorer ventana con la página de presentación solicitada.

> [!Note]  
> View **Service Desc.** la funcionalidad no está disponible en el código de ejemplo de C++.

 

**Para ver una descripción del servicio**

1.  Puede escribir la dirección URL de la descripción del servicio en **Service Desc. Campo de** dirección URL.

    ![dirección URL de descripción del servicio](images/ucp-url.png)

2.  Haga **clic en View Service Desc (Ver service Desc).** Se **muestra la ventana Visor de** descripción del servicio. A continuación, puede examinar la descripción del servicio mediante la vista de árbol. Esta funcionalidad no está disponible en el código de ejemplo de C++.

    ![ventana del visor de descripción del servicio](images/ucp-serv.png)

    Hay cinco comandos que puede usar en la ventana Visor de descripción del servicio.



| Botón                 | Acción realizada                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Go                     | Carga el archivo que se muestra en **Service Desc. Campo de** dirección URL.                                                                                                                              |
| Establecer acción             | Seleccione un nombre de acción en el árbol de descripción del servicio y haga clic **en Establecer acción.** El nombre de la acción se introduce en el **campo Acción** de invocación de la ventana **UCP genérica** principal.       |
| Establecer variable           | Seleccione un nombre de variable en el árbol de descripción del servicio y haga clic **en Establecer variable.** El nombre de la variable se introduce en el **campo Variable de** consulta de la ventana **UCP genérica** principal. |
| Rellenar lista de variables | Carga todos los nombres de variables del servicio en la **lista Variable de** consulta de la ventana principal **ucp** genérico.                                                                           |
| Rellenar lista de acciones   | Carga todos los nombres de acción del servicio en la lista **Acción** de invocación de la ventana **principal de UCP** genérico.                                                                              |



 

**Para controlar un dispositivo**

1.  En la **lista Dispositivos** encontrados, seleccione el dispositivo que desea controlar.
2.  En la **lista Elegir** servicio, seleccione el servicio que desea invocar o la variable de estado que desea consultar.

    ![ventana de dispositivos de control](images/ucp-contr.png)

    > [!Note]  
    > El contenido de la **lista de servicios** se basa en el dispositivo seleccionado en la lista **Dispositivos encontrados.**

     

3.  Si desea averiguar el valor de una variable de estado para el servicio seleccionado, escriba el nombre de la variable en el campo **Variable** de consulta del servicio. Haga clic en **Consulta**. Los resultados se muestran en el **campo Valor de estado de consulta/Argumentos de** salida de acción.
4.  Si desea invocar una acción para un servicio, escriba el nombre de la acción en el campo **Invocar** acción y los argumentos del campo **Argumentos de** acción. Haga clic **en Invocar**. Los resultados se muestran en el **campo Valor de estado de consulta/Argumentos** de salida de acción, si los hay.

    El valor devuelto, si existe, está incluido en el primer argumento out.

    > [!Note]  
    > Si hay varios argumentos para una acción, separelos con espacios.

     

5.  Vea la información de eventos en el **campo Eventos** del servicio seleccionado.

 

 




