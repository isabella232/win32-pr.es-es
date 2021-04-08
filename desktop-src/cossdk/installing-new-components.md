---
description: Para agregar componentes a la carpeta componentes de una aplicación COM+, puede utilizar el Asistente para instalación de componentes COM+ o arrastrar archivos. dll que contengan los componentes del explorador de Windows y colocarlos en la aplicación.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Instalación de nuevos componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080232"
---
# <a name="installing-new-components"></a>Instalación de nuevos componentes

Para agregar componentes a la carpeta **componentes** de una aplicación com+, puede utilizar el Asistente para instalación de componentes com+ o arrastrar archivos. dll que contengan los componentes del explorador de Windows y colocarlos en la aplicación.

Si usa el Asistente para instalación de componentes COM+, puede instalar un nuevo componente, que registra el componente en el equipo, o importar los componentes que ya se han registrado. Los componentes se pueden agregar a aplicaciones vacías o a aplicaciones existentes.

**Para agregar un componente a una aplicación COM+**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo que hospeda la aplicación COM+.

2.  Abra la carpeta **aplicaciones com+** para ese equipo y seleccione la aplicación en la que desea instalar los componentes.

3.  Abra la carpeta de la aplicación y seleccione **componentes**.

4.  En el menú **acción** , seleccione **nuevo** y, a continuación, haga clic en **componente**. También puede hacer clic con el botón secundario en la carpeta **componentes** , seleccionar **nuevo** y, a continuación, hacer clic en **componente**.

5.  En la página **principal** del Asistente para instalación de aplicaciones com+, haga clic en **siguiente** y, en el cuadro de diálogo **importar o instalar un componente** , haga clic en **instalar nuevos componentes** .

6.  En el cuadro de diálogo **instalar nuevos componentes** , haga clic en **Agregar** para buscar el componente que desee agregar.

7.  En el cuadro de diálogo **seleccionar archivos para instalar** , escriba el nombre de archivo del componente que se va a instalar o seleccione un nombre de archivo de la lista que se muestra. Haga clic en **Abrir**.

    Después de agregar los archivos, el cuadro de diálogo **instalar nuevos componentes** muestra los archivos que ha agregado y sus componentes asociados. Si activa la casilla **detalles** , verá más información sobre el contenido de los archivos y los componentes que se encontraron.

    > [!Note]  
    > Los componentes COM sin configurar deben tener una biblioteca de tipos. Si COM+ no encuentra la biblioteca de tipos del componente, el componente no aparecerá en la lista. También puede quitar un archivo de la lista **archivos para instalar** seleccionándolo y haciendo clic en **quitar**.

     

8.  Haga clic en **siguiente** y, a continuación, haga clic en **Finalizar** para instalar el componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Copiar componentes](copying-components.md)
</dt> <dt>

[Crear una nueva aplicación COM+](creating-a-new-com--application.md)
</dt> <dt>

[Eliminar una aplicación COM+](deleting-a-com--application.md)
</dt> <dt>

[Importar componentes](importing-components.md)
</dt> <dt>

[Mover componentes](moving-components.md)
</dt> <dt>

[Quitar un componente de una aplicación COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



